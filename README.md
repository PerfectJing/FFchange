I=imread('lena.tif');
ft=fft2(double(I));
tmp1=log(1+abs(ft));
spectrum=fftshift(ft);
tmp2=log(1+abs(spectrum));
ifcoef=ifft2(ft);

figure
subplot(221),imshow(I),title('source image');
subplot(222),imshow(tmp1,[]),title('FFT image');
subplot(223),imshow(tmp2,[]),title('shift FFT image');
subplot(224),imshow(ifcoef,[]),title('IFFT image');
