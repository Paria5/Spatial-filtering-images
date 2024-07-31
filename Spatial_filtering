clear all
clc
a=imread('sample.JPG');
imshow(a)
figure
h=3;
b=rgb2gray(a);
imshow(b)
figure
b(size(b,1)+h-1,size(b,2)+h-1)=0;
c=circshift(b,[1 1]);

for k=1:(size(a,1)-1)
      for m=1:(size(a,2)-1)
          for i=k:k+h-1
             for j=m:m+h-1
             e(i,j)=c(i,j)*(1/h^2);
             end
          end
       f=sum(sum(e));
       if sum(f)>256
           g(k+1,m+1)=256;
       else
           g(k+1,m+1)=uint8(f);
       end
       e=[];
      end
end
imshow(g)

