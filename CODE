original=imread('/Users/rachanagb/Desktop/Images/origianl_pcb.JPG');
original_copy=original;
test=imread('/Users/rachanagb/Desktop/Images/01_open_circuit_01.jpg');
test_copy=test;

%enhancing and denoising
original=histeq(im2gray(original));
original=imgaussfilt(original,0.06);
test=histeq(im2gray(test));
test=imgaussfilt(test,0.06);

%binarising
thershold=75;
image_binarise=original>thershold;
test_binarise=test>thershold;

%noise removal in binarised image
image_denoise=medfilt2(image_binarise,[12,12]);
test_denoise=medfilt2(test_binarise,[12,12]);

%structural element
structure=strel('disk',3);

%hole detection
image_final=imopen(image_denoise,structure);
test_final=imopen(test_denoise,structure);
difference=medfilt2((xor(image_final,test_final)),[21,21]);

%open circuit detection
image_dilate=imdilate(image_denoise,structure);
test_dilate=imdilate(test_denoise,structure);
difference1=medfilt2((xor(image_dilate,test_dilate)),[17,17]);

%display
subplot(1,3,1);
imshow(original_copy);
title("original pcb with no defects");
subplot(1,3,2);
imshow(test_copy);
title("defect pcb");

%applying bounding boxes for holes and open circuit
if(difference==0)
cordinates1=regionprops(difference1,'BoundingBox');

subplot(1,3,3);
imshow(test_copy);
title("defect detected:Open Circuit");
hold on;
for j=1:length(cordinates1)
boundary=cordinates1(j).BoundingBox;
rectangle('Position',[boundary(1),boundary(2),boundary(3),boundary(4)],'EdgeColor','g','LineWidth',1);
end
hold off;
else
cordinates=regionprops(difference,'BoundingBox');
subplot(1,3,3)
imshow(test_copy);
title("defect detected:circuit with missing holes");
hold on;
for k=1:length(cordinates)
thisBB=cordinates(k).BoundingBox;
rectangle('Position',[thisBB(1),thisBB(2),thisBB(3),thisBB(4)],'EdgeColor','r','LineWidth',1);
end
hold off;
end
