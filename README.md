# Stef

Exercitiul 1

function Ex1()

Fs = 5000;
t = 0:1/Fs:100;

x = square(pi*t,25);%generez un semnal dreptunghiular

for i = 1:1:length(x)
   if x(i) > 0
       x(i) = x(i)/2;
   end
end

plot(t,x)
axis([0 5.2 -1.2 1.2])
xlabel('Timp (sec)')
ylabel('Amplitude')
title('Semnal Dreptunghiular')

end


Exercitiul 2

function Ex2()

Fs = 2000;
T = 0:1/Fs:100;
x = sawtooth(0.4*pi*T, 0.5);%generez un semnal triunghiular
plot(T,x);


xlabel('Timp (sec)')
ylabel('Amplitude')
title(' Semnal Triunghiular')

end


Exercitiul 3

function Ex3(s)
    N = 4;
    Ts = 0.001;
    T = 0:Ts:N;
    
    k = 1;
    
    for i = 1:length(T)
     if  T(i) <= k*0.25
         if k <= length(s)
             x(i) = s(k);
         else
             x(i) = 0;
         end
     else
        if k <= length(s)
             x(i) = s(k);
        end
        k = k+1; 
     end
    end
    
    axis([0 20 -5 3])
    plot(T,x);
   
end


Exercitiul 4

T1=0:0.2:10;
S1=0.8*sin(2*pi*0.333*T1);
for i=1:1:length(S1);      
    if S1(i)<0;
        S1(i)=0;
    end
end
subplot(3,1,1)
plot(T1,S1),grid
xlabel('Timp(sec)')
ylabel('Amplitude')

T2=0:0.02:10;
S2=0.8*sin(2*pi*0.333*T2);
for i=1:1:length(S2);
    if S2(i)<0;
        S2(i)=0;
    end
end
subplot(3,1,2)
plot(T2,S2),grid
xlabel('Timp(sec)')
ylabel('Amplitude')


T3=0:0.002:10;
S3=0.8*sin(2*pi*0.333*T3);
for i=1:1:length(S3);
    if S3(i)<0;
        S3(i)=0;
    end
end
subplot(3,1,3)
plot(T3,S3),grid
xlabel('Timp(sec)')
ylabel('Amplitude')


Exercitiul 5

T1= 0:0.2:10;                   
S1=abs(1.5*sin(2*pi*0.25*T1)); 
subplot(3,1,1)
plot(T1,S1),grid
xlabel('Timp(sec)')
ylabel('Amplitude')

T2=0:0.02:10;
S2=abs(1.5*sin(2*pi*0.25*T2));
subplot(3,1,2)
plot(T2,S2),grid
xlabel('Timp(sec)')
ylabel('Amplitude')

T3=0:0.002:10;
S3=abs(1.5*sin(2*pi*0.25*T3));
subplot(3,1,3)
plot(T3,S3),grid
xlabel('Timp(sec)')
ylabel('Amplitude')


    
