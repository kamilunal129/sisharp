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

Kullanıcıdan 20 adet sayı girmesi istenecek, sayılar diziye kaydedilecek ve girilen sayıları dizi
halinde büyükten küçüğe ve küçükten büyüğe sıralayan programı yazınız

{
        static void Main(string[] args)
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

==============================================================================================

