# **C++ Notlarım**

(Son güncelleme: 21/05/2023)

Türkçe c++ notlarıma hoş geldin. C++ notlarımı aktarırken aklına takılan herhangi bir noktayı sormaktan çekinme.

Öğrendiklerim arasında kendi yorumum bulunmaktadır. Bu yüzden yanlış olduğunu düşündüğün bir nokta varsa muhakkak ulaş bana. Hata yapmış olabilirim :)

Her geçen gün yeni bir bilgi öğrendiğimden notlar güncellenebilir :)

- [**C++ Notlarım İçindekiler**](#c-notlarım)
  
  - [Hello World!](#hello-world)
  - [Yorum(Comment) Ekleme](#yorumcomment-ekleme)
  - [Değişkenler(Variables) ve Tanımlama ](#de%C4%9Fi%C5%9Fkenlervariables-ve-tan%C4%B1mlama)
  - [Değişken İsimleri ve Belirleyiciler Identifiers](#değişken-i̇simleri-ve-belirleyiciler-identifiers)
  - [Değişken Tipleri](#değişken-tipleri)
  - [ASCII Tablosu](#ascii-tablosu)
  - [Tip Dönüşümleri](#tip-dönüşümleri)
  - [İşlemler - Operatörler](#i̇şlemler-operatörler)
  - [Temel Giriş ve Çıkış İşlemleri (cin ve cout)](#temel-giriş-ve-çıkış-i̇şlemleri-cin-ve-cout)
## Hello World

Her satırın sonuna ; koymalısın. C++'da bu satırın bittiğini ifade eder.

#include : belirtilen dosyayı kodun yazıldığı dosya içerisine eklemek için kullanılır. Eğer belirtilen dosya yok ise ekrana bir uyarı mesajı verir.

"< iostream >" : Standart akışlardan okuma ve yazma denetimi sağlayan nesneleri bildirir. Bu genellikle C++ programından giriş ve çıkış yapmak için ihtiyacınız olan tek üst bilgidir.
(kişisel yorum: kütüphanedir ve bazı temel şeyleri yazmamızı sağlar)

[Ekşi Sözlükte yapılan basit bir tanım](https://eksisozluk2023.com/iostream--335972) : input ve output icin include edilen header. yani kullaniciya bir yazi gosterecegimiz zaman yada kullanicidan bir yazi alacagimiz zaman kullaniriz. c++ in hello world orneginde karsimiza cikar. #include using namespace std; void main() { cout << "hello world!" ; }

"cout << "hello world!" ;" satirinda de cout u kullanabilmemiz icin include etmemiz lazimdir. programlamaya basladigim zaman bunun daha basit bir tanimini aradim hello world orneginde. fakat bulamadim. hayatinda ilk defa kod goren birinin anlamadigi bir #include gormesi pek hos degil. simdi benim yapabilecegim en basit tanim budur.


```
#include <iostream> 
using namespace std; 
int main() {
cout << "Hello World!;
reurn 0;
}
```
  ```cout << ''Hello World!'' << endl;``` şeklinde de yazılabilirdi. Endl;; end line yani satır sonu demektir ve ekrana yazdırılan çıktının ardından görüntülenecek veriyi bir alt satırda görüntülemeye yarar. 
  
```return 0;``` satırının genel kabul görmüş manası da "Program hatasız sonlandırıldı" demek oluyor.  

## Yorum(Comment) Ekleme

![https://github.com/eyupece/cpp-note/blob/main/o7oz5ph.png](./o7oz5ph.png "GitHub")

// kullanılırsa o satır yokmuş gibi hareket edilir. 

Eğer birden fazla satırda sürekli // kullanmak istemiyorsak /* yapıp yorumu bitirmek istediğimizde */ yaparsak oradaki yorum da kodda gözükmez. Yorum olarak kalır. Bazı programlarda /* ifadesinden sonra her satırın başında * olabilir olup olmaması önemli değil. 

 ## Değişkenler(Variables) ve Tanımlama 
```
#include <iostream>
using namespace std;

int main()
{
int a; // tipi integer, ismi a

 a = 10; //değer
// variable degisken olarak da gecer
a = 20  /* atama, assignment. buradaki = matematikteki gibi değil.
Sağdaki değeri al soldakinin içine koy gibi bir tanım mevcut.
ilk önce a'nın içine 10 koyduk sonra 20 koyduk son koyulan değer geçerlidir */;

  cout << a << endl;
  ```
Burada Çıktı 20'dir.
```
#iclude <iostream>
using namespace std;

main()
{
int a = 10, b = 2, z; /* a isminde bir değişken tanımla ve değerini 10 yap, b adında bir değişken tanımla 2 yap ve < adında değişken tanımla */
cout << z << endl; 
  //z'nin değeri tanımlanmadığı için hata verecektir 
  cout << a << b << endl;
  }
  ```

## Değişken İsimleri ve Belirleyiciler Identifiers 

![https://github.com/eyupece/cpp-note/blob/main/belirleyiciler.png](./belirleyiciler.png "GitHub")

Sembollerden sadece _ ile başlayabilir 

## Değişken Tipleri

![https://github.com/eyupece/cpp-note/blob/main/degisken-tipleri.png](./degisken-tipleri.png "GitHub")

Float: Ondalıklı sayı 3.14 

Boolean: 0-1 True-False  

Void:Tipsiz. Ne olduğu bilinmiyorsa kullanılır 

Null: boş 

## ASCII Tablosu

![https://github.com/eyupece/cpp-note/blob/main/ASCII%20TABLE.png.png](./ASCII%20TABLE.png "GitHub")


## Tip Dönüşümleri 

**char -> integer : ** 
```
#include <iostream>
using namespace std;

int main()
{
	int a = 10;
	float pi = 3.14;
	long tl = 327462384634783; 
  char b = 'x';
	
	cout << a << endl;
	cout << pi << endl; cout << tl << endl;
	cout << b << endl;
	
	int cc = b;
	cout << cc << endl;

	return 0;
}
```
Terminal :
```
10
3.14
1193085855
x
120
```
120'nin sebebi ASCII Tablosu
Her karakter bir sayıdır. Char'da bahsi geçen harfleri integer'a çevirdiğinden dolayı decimala çevirir.  
X->120 

**float -> integer :** 
```
#include <iostream>
using namespace std;

int main()
{
	int a = 10;
	float pi = 3.14;
	long tl = 327462384634783; 
  char b = 'x';
	
	cout << a << endl;
	cout << pi << endl; cout << tl << endl;
	cout << b << endl;
	
	int cc = b;
	cout << cc << endl;
  
  int ipi = pi;
  cout << ipi << endl; // 3

	return 0;
}
```
Son satırdaki float -> integer dönüşümünde sonuç 3 çıkar.

Normalde pi 3.14 bu yüzden floatla yazdık fakat ipi olarak tanımlarsak ve integer olarak yazarsak ondalıklı kısmını atıp 3 olarak çıkarır.

Kendiniz değer girip uygulama yaparsanız daha etkili sonuç elde edersiniz.
 
 **integer -> float :** 
```
int birsayi= 5;
float sayi2 = birsayi; 
cout << sayi2 << endl; // Sonuç 5 Çıkar
```
**integer -> char :**
```
int sayiint = 37; 
char sayiiyeni = sayiint; 
cout << sayiiyeni << endl; // Sonuç % çıkar
```
Sonucu ASCII tablosundan test et

***KESTİRME BASİT YOL :***
```
int yenisayi = 35; 
 cout << (char) yenisayi << endl; // Sonuç # çıkar
```
İfade edildiği gibi cout <<(int,char,float vb.)identifier << endl; 

Şeklinde daha kısa yazmak mümkün 

Buna *Type casting* denir 

## İşlemler (Operatörler)

![https://github.com/eyupece/cpp-note/blob/main/islemler.png](./islemler.png "GitHub")

**Complement " ~ "** ikilik sistemde 0ları 1 ,1 leri 0 yap demektir. 
```
#include <iostream>
using namespace std;

int main() {

	int a = 10;
	 cout << a << endl; 

	a++; //bir arttır demek posfix
	 cout << a << endl;

	++a; //bir tane daha arttıracağız increment prefix
	 cout << a << endl; //a en son 12 oldu b'yi de 20 diye tamamladık

	int b = 20;
     cout << a + b << endl;
     cout << 10 + 3 * 5 << endl; //işlem önceliği vardır.
	// * + - /
	 cout << 7 % 5 << endl; // remainder, modulo 34 3 4 gibi kalanı ifade eder

	a--; //a'nın değerini bir azalt, a en son 12ydi 11 oldu
    a = a - 1; // ilk derslerde ='in matematiksel olmadığını belirttik. Bu ifade a'ya bir azalt demektir a = 10 olur
    cout << a << endl;

	return 0;
}
```
	
Terminal
```
10
11
12
32
25
2
10
```	
-----------------------------------------------------------

***++a ile a++ kıyası***

```
/* ++a; a++; 
bu iki ifade arasında bu kullanımda fark yok a'nın değeri 12 */

cout << a++ << endl; /* a'nın değeri denkleme alınır 
sonra bir arttırılır yani aslında bu 10u basıp sonra 11 yapıyor o yüzden 10 gözüküyor */

cout << ++a << endl; /* a'nın değeri önce arttırılır sonra denkleme eklenir. 
Yani aslında burada da 11di once 1 arttırıp 12 yapıyor sonra 12 olarak basıyor */ 
//bu iki ifade arasında fark var
```
Terminal 
```
10
10 
12
```

--------------------------------------------------------------

```
int x = 10;
x--;
x = x - 1; // iki ifade aynı hatta tek başına yazılırsa --x de bunlarla aynı 
x -= 1; // bu ifade yukarıda yer alan ifadenin kısaltılmış halidir
x += 6; // x = x+6 demektir
x *= 2; // x = x*2

cout << x << < endl; // Sonuç 26
```

## Left Shift & Right Shift

![https://github.com/eyupece/cpp-note/blob/main/leftshift.png](./leftshift.png "GitHub")


![https://github.com/eyupece/cpp-note/blob/main/leftshiftt.png](./leftshiftt.png "GitHub")

Iki kaydır demek binary sistemde  aynen yaz sonuna iki 0 ekle demektir. Sonrasında onluk sisteme geri geçilir. 


![https://github.com/eyupece/cpp-note/blob/main/rightshift.png](./rightshift.png "GitHub")

![https://github.com/eyupece/cpp-note/blob/main/rightshiftt.png](./rightshiftt.png "GitHub")

Right shiftte sonda 0 yoksa diğer basamaklar silinir 

![https://github.com/eyupece/cpp-note/blob/main/bitwiseorn.png](./bitwiseorn.png "GitHub")

![https://github.com/eyupece/cpp-note/blob/main/bitwiseornn.png](./bitwiseornn.png "GitHub")

Tabii ki bu örneklerler yetinmemelisiniz. Lütfen sayıları ve [operatörleri](#i̇şlemler-operatörler) değiştirip yeni yeni örnekler yapın. DAha iyi oturacaktır.


## Temel Giriş ve Çıkış İşlemleri (cin ve cout)

***Standart output:*** monitör 

***Standart input :*** klavye olarak düşünülmeli

C input(cin) 

C output(cout) 

```
#include <iostream>
using namespace std;

int main()
{
int x = 10;
cout << x << endl;

cin >> x; // bu komut klavyeden girilen değeri okur
cout << "klavyeden " << x << " degerini girdiniz" << endl; /*türkçe harf kullanma 
Ayrıca kelimelerin bitişik olmaması için sonların ve başlarına boşluk koy */ 
cout << "klavyede girilen degerin 10 fazlasi " << x+10 << " olur" << endl;

return 0;
}
```
Terminal
```
10
70
klavyeden 70 degerini girdiniz
klavyede girilen degerin 10 fazlasi 80 olur
```
	
