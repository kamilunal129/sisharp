# sisharp
C# Problems
C#  Otopark Programı
{
 ## Bir otoparka park eden taksinin 1 saati 5TL, minibüsün 1 saati 6TL, ticari aracın 1 saati 6.5TL dir. Taksi 1 saatten sonraki her saat başı için %20 daha fazla, minibüs 1 saatten sonraki her saat başı için toplamda %21.5 ve ticari araç 1 saatten sonraki her saat başı için toplamda %25 daha fazla ödeme yapmaktadır. Buna göre klavyeden girilen araba tipi ve kalınan saat bilgisi girildikten sonra ekrana ödenecek otopark ücretini hesaplayan programın kodlarını yazınız.

  
            double odenecekTutar = 0;
            
            int kalinanSure = 0, aracTipi = 0;
            Console.WriteLine("Araç Tipleri Taksi : 1, Minübüs : 2, Ticari : 3");
            Console.Write("Lütfen Araç Tipini Giriniz : ");
            aracTipi = Convert.ToInt32(Console.ReadLine());
            Console.Write("Kalınan Süreyi Giriniz : ");
            kalinanSure = Convert.ToInt32(Console.ReadLine());
            if (kalinanSure > 1)
            {
                for (int i = 1; i <= kalinanSure; i++)
                {
                    if (i == 1) {
                        if (aracTipi == 1) { odenecekTutar = i * 5; }
                        else if (aracTipi == 2) { odenecekTutar = i * 6; }
                        else if (aracTipi == 3) { odenecekTutar = i * 6.5; }
                    }
                    else {
  
                        kalinanSure -= 1;
                        if (aracTipi == 1) { odenecekTutar+= kalinanSure * 5 * 1.20; }
                        else if (aracTipi == 2) { odenecekTutar+= kalinanSure * 6 * 1.215; }
                        else if (aracTipi == 3) { odenecekTutar+= kalinanSure * 6.5 * 1.25; }
                    }
                }
  
  
            }
  
  
            else {
  
                if (aracTipi == 1) { odenecekTutar = kalinanSure * 5; }
                else if (aracTipi == 2) { odenecekTutar = kalinanSure * 6; }
                else if (aracTipi == 3) { odenecekTutar = kalinanSure * 6.5; }
                  
              
            }
            Console.WriteLine("Ödenecek Tutar : {0} TL",odenecekTutar);
      
  }  

==========================================================================================
Üç katlı bir bina her katında iki daire var klavyeden her dairede bulunan kişi sayısını
girdikten sonra binada kaç kişi olduğunu hesaplayan programın kodlarını yazın.

int[,] dizi = new int[3, 2];
int toplamKisi = 0, evdekiKisi = 0;
for (int i = 0; i < dizi.GetLength(0); i++)
{
for (int y = 0; y < dizi.GetLength(1); y++)
{
 
Console.Write("{0}. Kat {1}. Dairedeki Kişi sayısını Giriniz : ",i+1,y+1);
evdekiKisi = Convert.ToInt32(Console.ReadLine());
toplamKisi += evdekiKisi;
}
}
Console.WriteLine("Toplam Kişi Sayısı : {0}",toplamKisi);

==========================================================================================

Bir Dik üçgende hipotenüsün uzunluğunun karesi, dik kenarların uzunluklarının
kareleri toplamına eşittir. Bu bağıntıya (Pythagoras) Pisagor Bağıntısı denir.
Hipotenüs 90 derecenin karşısındaki kenardır. Dik kenarlar ise 90 derecenin oluştuğu
kenarlardır. Klavyeden girilen b ve c değerlerine göre a ‘ yı bulup ekrana yazan programın
kodlarını yazınız.

            double  a,b,c;
            Console.Write(“b değerini giriniz : “);
            b =double.Parse(Console.ReadLine());
            Console.Write(“c değerini giriniz : “);
            c = double.Parse(Console.ReadLine());
            a = Math.Sqrt((Math.Pow(b, 2) + Math.Pow(c, 2)));
            Console.WriteLine(“Sonuc {0}”,a);
            Console.ReadKey();

==============================================================================================

0 dan klavyeden girilen sayıya kadar olan sayılardan; tek olanları tek sayılar dizisine, çift olanları
çift sayılar dizisine saklayan ve bu dizileri ayrı ayrı ekrana yazdıran program.

          ArrayList tekSayilar = new ArrayList();
          ArrayList ciftSayilar = new ArrayList();
          Console.Write("Bir Sayı Giriniz : ");
          int sayi = Convert.ToInt16(Console.ReadLine());
          for (int i = 0; i <= sayi; i++)
          if (i % 2 == 0) //sayımız çift sayı ise çift sayılar dizisine ekleniyor  
ciftSayilar.Add(i);  
    else  //aksi durumda tek sayılar dizisine ekleniyor  
       tekSayilar.Add(i);  
  
 Console.WriteLine("Tek Sayılar Dizisi Listeleniyor ... ");  
 for (int i = 0; i < tekSayilar.Count; i++)  
    Console.WriteLine(tekSayilar[i]);  
  
   Console.WriteLine(" ");  
  
 Console.WriteLine("Çift Sayılar Dizisi Listeleniyor ... ");  
 for (int i = 0; i < ciftSayilar.Count; i++)  
    Console.WriteLine(ciftSayilar[i]);  
   
 Console.ReadKey(); 

==============================================================================================
fibonacci

namespace orn1061
{
class Class1
{
static int fibonacci(int n)
{
int i,terim=0;
if(n==1) terim=1;
else if(n==2) terim=1;
else for(i=3;i<=n;i++)terim=fibonacci(i-1)+fibonacci(i2);
return terim;
}
static void Main(string[] args)
{
int x,sonuc;
Console.Write("terim numarası=");
x=Convert.ToInt32(Console.ReadLine());
sonuc =fibonacci(x);
Console.WriteLine("dizinin terimi={0}", sonuc);
Console.ReadLine();
}
}
}

==============================================================================================

Kullanıcıdan 20 adet sayı girmesi istenecek, sayılar diziye kaydedilecek ve girilen sayıları dizi
halinde büyükten küçüğe ve küçükten büyüğe sıralayan programı yazınız

        {
        static void Main(string [] args)
        {
         int enbuyuk = 0;
         int enkucuk = 100;
         int sayi;
         for (int i = 1; i < 21; i++)
         {
          Console.Write(i+". sayıyı giriniz= ");
          sayi = Convert.ToInt32(Console.ReadLine());
          if (sayi < enkucuk) enkucuk = sayi; if (sayi &gt; enbuyuk)
          enbuyuk = sayi;
          }
          Console.WriteLine("En büyük sayı= "+enbuyuk);
          Console.WriteLine("En küçük sayı= " + enkucuk);
          Console.ReadKey();
          }
          }

==========================================================================================

Selsiyus türünde sıcaklık verildiğinde fahrenhayt türünde sıcaklığı hesaplayan program

        class Program
        {
        static void Main(string[] args)
        {
        int celsius, faren;
        Console.Write("Santigrat Girin(°C) : ");
        celsius = int.Parse(Console.ReadLine());
        faren = (celsius * 9) / 5 + 32;
        Console.WriteLine("Fahrenhayt : {0} (°F) ", faren);
        Console.ReadLine();
 
         }}

==========================================================================================

Girilen TC kimlik numarasının doğru olup olmadığını bulan programı yazınız


 class Program
    {
        static void Main(string[] args)
        {
            string tcKimlikNo = Console.ReadLine();
            bool returnvalue = false;
            if (tcKimlikNo.Length == 11)
            {
                Int64 ATCNO, BTCNO, TcNo;
                long C1, C2, C3, C4, C5, C6, C7, C8, C9, Q1, Q2;
 
                TcNo = Int64.Parse(tcKimlikNo);
 
                ATCNO = TcNo / 100;
                BTCNO = TcNo / 100;
 
                C1 = ATCNO % 10; ATCNO = ATCNO / 10;
                C2 = ATCNO % 10; ATCNO = ATCNO / 10;
                C3 = ATCNO % 10; ATCNO = ATCNO / 10;
                C4 = ATCNO % 10; ATCNO = ATCNO / 10;
                C5 = ATCNO % 10; ATCNO = ATCNO / 10;
                C6 = ATCNO % 10; ATCNO = ATCNO / 10;
                C7 = ATCNO % 10; ATCNO = ATCNO / 10;
                C8 = ATCNO % 10; ATCNO = ATCNO / 10;
                C9 = ATCNO % 10; ATCNO = ATCNO / 10;
                Q1 = ((10 - ((((C1 + C3 + C5 + C7 + C9) * 3) + (C2 + C4 + C6 + C8)) % 10)) % 10);
                Q2 = ((10 - (((((C2 + C4 + C6 + C8) + Q1) * 3) + (C1 + C3 + C5 + C7 + C9)) % 10)) % 10);
 
                returnvalue = ((BTCNO * 100) + (Q1 * 10) + Q2 == TcNo);
            }
           
 
            if (returnvalue)
                Console.WriteLine("Doğru");
            else
                Console.WriteLine("Yanlış");
            Console.ReadKey();
        }
    }
    
  ==========================================================================================
  
  Bir komisyoncu sattığı mallardan fiyatı 50 TL kadar olanlardan %3, daha fazla olanlardan ise
%2 komisyon almaktadır. Klavyeden teker teker girilen 5 malın komisyonlarını bulup ekrana
yazdıran ve en sonunda da toplam komisyonu ekrana yazdıran programın c# console
uygulaması kodlarını yazınız.

    double malFiyati = 0, komisyonMiktari = 0,toplamKomisyon=0;
for (int i = 0; i < 5; i++)
{
Console.Write("{0}. Malın Fiyatını Giriniz : ",i+1);
malFiyati = Convert.ToDouble(Console.ReadLine());
if (malFiyati > 50) komisyonMiktari = malFiyati * 0.02;
else komisyonMiktari = malFiyati * 0.03;
Console.WriteLine("{0}. Mal İçin Komisyon Miktarı : {1}",i+1,komisyonMiktari);
toplamKomisyon += komisyonMiktari;
}
Console.WriteLine("Toplam Komisyon Miktarı : {0}",toplamKomisyon);

============================================================================================
Bir konfeksiyon imalathanesi; pantolonu 1,2m kumaş kullanarak 4 saatte tamamlayıp 16 tl ’ye
satmaktadır. Takım elbiseyi ise 2,8m kumaş kullanarak 15 saatte tamamlayıp 50 tl ’ye satmaktadır. İşletme
kumaşın metresini 8 tl ’ye almaktadır. Buna göre işletmede üretilmesi gereken pantolon ve takım elbise
sayısı verildiğinde; gerekli olan kumaş miktarı, kumaş için ödediği para, kazandığı para ve toplam çalışma
sürelerini hesaplayan program yazınız

using System;
namespace orn1012
{
class Class1
{
static void Main(string[] args)
{
int ps,tks;
double tpkumas,kmfiyat,sure,gelir;
Console.WriteLine("pantolon sayısı:");
ps=Convert.ToInt32(Console.ReadLine());
Console.WriteLine("takım elbise sayısı:");
tks=Convert.ToInt32(Console.ReadLine());
tpkumas=ps*1.2+tks*2.8;
kmfiyat=tpkumas*8;
sure=ps*4+tks*15;
gelir=ps*16+tks*50;
Console.WriteLine("toplam kumaş miktarı={0} m",tpkumas);
Console.WriteLine("toplam çalışma süresi={0} saat",sure);
Console.WriteLine("kumaş için ödenen para={0}
ytl",kmfiyat);
Console.WriteLine("elde edilecek gelir={0} ytl",gelir);
Console.ReadLine();
}
}
}

=================================================================================================
Bir deney ortamındaki belirli bir molekülün kütlesi her gün belirli oranda artmaktadır. Bu ortamda ilk
gündeki molekül kütlesi son gündeki molekül kütlesi ve günlük artış yüzdesi verildiğinde geçen gün
sayısını hesaplayan program

using System;
namespace orn1019
{
class Class1
{
static void Main(string[] args)
{
double ilk,son,n;
double n1,yuzde;
Console.WriteLine("başlangıçtaki molekül kütlesi:");
ilk=Convert.ToDouble(Console.ReadLine());
Console.WriteLine("sondaki molekül kütlesi:");
son=Convert.ToDouble(Console.ReadLine());
Console.WriteLine("günlük artış yüzdesi:");
yuzde=Convert.ToDouble(Console.ReadLine());
n=(Math.Log10(son)-
Math.Log10(ilk))/Math.Log10(1+yuzde/100);
n1=Math.Floor(n);
Console.WriteLine("Gün sayısı:{0}",n1);
Console.ReadLine();
}
}
}
=========================================================================
50 km uzunluğunda bir yol yapımı işinin başlama maliyeti 50000 tl’dir. Ayrıca yapılacak yolun ilk 15
km kısmında km başına 2000 tlyapım maliyeti, 16. km ile 40. km arasında km başına 2400 tlyapım
maliyeti ve 41. km’den itibaren km başına 1950 tlyapım maliyeti vardır.Bu yol yapımı işinde; yapımı
bitirilen yol km olarak verildiğinde toplam gelinen aşamaya kadar olan toplam maliyeti hesaplayan
program yazınız


using System;
namespace orn1057
{
class Class1
{
static void Main(string[] args)
{
double yol,maliyet;
Console.Write("yapılan yol miktarı:");
yol=Convert.ToDouble(Console.ReadLine());
if(yol<0)
Console.WriteLine("yol miktarı yanlış girildi.");
else if(yol<=15)
{
maliyet=50000+yol*2000;
Console.WriteLine("toplam maliyet={0}",maliyet);
}
else if(yol<=40)
{
maliyet=80000+(yol-15)*2400;
Console.WriteLine("toplam maliyet={0}",maliyet);
}
else if(yol<=50)
{
maliyet=140000+(yol-40)*1900;
Console.WriteLine("toplam maliyet={0}",maliyet);
}
else
Console.WriteLine("yol miktarı yanlış girildi.");
Console.ReadLine();
}
}
}

=======================================================================
 Bir üretim merkezine her 30 dakikada bir A ve B hammaddeleri gelmektedir. A hammaddesinden 5
birim ve B hammaddesinden 7 birim alındığında 1 birim C ürünü elde edilmektedir. Üretim merkezi 24
saat çalıştığında; her 30 dakikada bir gelen hammadde miktarları verildiğinde süre sonunda üretilen C
ürünü sayısını, artan A ve B hammaddeleri miktarlarını bulan program yazınız. Üretim merkezi 30
dakika bir gelen hammaddeleri işleme kapasitesindedir.

namespace orn1049
{
class Class1
{
static void Main(string[] args)
{
int a,b,c,i;
int toplam_a,toplam_b;
int artan_a,artan_b;
toplam_a=0;
toplam_b=0;
for(i=1;i<=48;i++)
{
Console.Write("A maddesi miktarını giriniz:");
a=Convert.ToInt32(Console.ReadLine());
Console.Write("B maddesi miktarını giriniz:");
b=Convert.ToInt32(Console.ReadLine());
toplam_a=toplam_a+a;
toplam_b=toplam_b+b;
}
c=(toplam_a/5<toplam_b/7)?toplam_a/5:toplam_b/7;
artan_a=toplam_a-c*5;
artan_b=toplam_b-c*7;
Console.WriteLine("toplam A maddesi miktarı={0}
birim",toplam_a);
Console.WriteLine("toplam B maddesi miktarı={0}
birim",toplam_b);
Console.WriteLine("C maddesi miktarı={0} birim",c);
Console.WriteLine("artan A maddesi miktarı={0}
birim",artan_a);
Console.WriteLine("artan B maddesi miktarı={0}
birim",artan_b);
Console.ReadLine();
}
}
}

=======================================================================

Bir imalathanede iki çeşit ürün (X ve Y) için iki üretim tezgâhı (A ve B) kullanılmaktadır. X ürünü
için; A tezgâhı 3 saat, B tezgâhı 2 saat ve Y ürünü için; A tezgâhı 4 saat, B tezgâhı 7 saat çalışmaktadır

static void Main(string[] args)
{
 double AMaliyet, BMaliyet, ASure, BSure;
 int x, y;
 Console.Write("X ürünü adedi :");
 x = Convert.ToInt32(Console.ReadLine());
 Console.Write("Y ürünü adedi :");
 y = Convert.ToInt32(Console.ReadLine());
 ASure = 3 * x + 4 * y;
 BSure = 2 * x + 7 * y;
 AMaliyet = 12.45 * ASure;
 BMaliyet = 18.23 * BSure;
 Console.WriteLine("A tezgahının:\nKullanılma süresi :{0} saat", ASure);
 Console.WriteLine("Maliyeti :{0} lira", AMaliyet);
 Console.WriteLine("B tezgahının:\nKullanılma süresi :{0} saat", BSure);
 Console.WriteLine("Maliyeti :{0} lira", BMaliyet);
 Console.ReadLine();
}

