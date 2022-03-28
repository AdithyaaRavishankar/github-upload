int main(){
int n,i,a[5000],b[5000],min=a[0],steps=0,f=0;
scanf("%d",&n);
for(i=0;i<n;i++) scanf("%d",&a[i]);
for(i=0;i<n;i++) scanf("%d",&b[i]);
min=a[0];
for(i=1;i<n;i++){
     if(a[i]<min)min=a[i];
}
for(i=0;i<n;i++){
   while(a[i]>min && b[i]!=0){
        a[i]-=b[i];
        steps++;
    }
   if(a[i]<0){
    f=1;
     break;
    }
     if(a[i]<min){
     min=a[i];
      i=-1;
     }
     }
if(f!=1) printf("%d",steps);
else printf("-1");
}