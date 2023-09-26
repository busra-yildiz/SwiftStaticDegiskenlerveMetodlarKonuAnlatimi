# SwiftStaticDegiskenlerveMetodlarKonuAnlatimi
Swift programlama dilinde "static" kelimesi, sınıflara ait belirli özelliklerin ve metodların sınıfa özgü olduğunu ve sınıfın herhangi bir 
örneği oluşturulmadan doğrudan sınıf adı üzerinden erişilebileceğini belirtmek için kullanılır. İşte Swift'te static değişkenler ve metodlar hakkında
daha fazla bilgi:

Static Değişkenler (Static Variables):

Static değişkenler, bir sınıfın her örneği için aynı değere sahip olan değişkenlerdir. Bu değişkenlere, her örneğin kendi kopyasını almadığı
bir değer atandığında kullanışlıdır. Static değişkenler sınıfın kendisine aittir ve sınıf adı üzerinden erişilirler.

Örnek:
class Araba {
    static var uretilenArabaSayisi = 0
    
    init() {
        Araba.uretilenArabaSayisi += 1
    }
}

Bu örnekte, uretilenArabaSayisi isimli static bir değişken tanımlanmıştır. Bu değişken, her yeni Araba örneği oluşturulduğunda arttırılır.

Static Metodlar (Static Methods):

Static metodlar, bir sınıfın örnekleri olmadan çağrılabilen metotlardır. Bu, belirli bir sınıfın işlevselliğini sınıf adı üzerinden 
kullanmanıza olanak tanır.

Örnek:

class Matematik {
    static func topla(_ sayi1: Int, _ sayi2: Int) -> Int {
        return sayi1 + sayi2
    }
}

Bu örnekte, topla isimli bir static metot tanımlanmıştır. Bu metot, iki sayıyı toplar ve sonucu döndürür. 
Herhangi bir Matematik örneği oluşturmadan bu metotu çağırabilirsiniz.

Static Kullanımı:

Static değişkenlere ve metodlara sınıf adı üzerinden erişilir. Örneğin:

let araba1 = Araba()
print(Araba.uretilenArabaSayisi) // 1

let araba2 = Araba()
print(Araba.uretilenArabaSayisi) // 2

let toplam = Matematik.topla(5, 3)
print(toplam) // 8

Bu örnekte, Araba sınıfının static değişkenine ve Matematik sınıfının static metoduna doğrudan sınıf adı üzerinden erişiyoruz.

Static değişkenler ve metodlar, özellikle belirli bir sınıfın örneği olmadan kullanmanız gereken işlevselliği tanımlarken kullanışlıdır. 
Bu, belirli verileri paylaşmak veya belirli işlemleri gerçekleştirmek için kullanılabilir.
