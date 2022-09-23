# Automation-java

import io.github.bonigarcia.wdm.WebDriverManager;
import org.junit.AfterClass;
import org.junit.Assert;
import org.junit.BeforeClass;
import org.junit.Test;
import org.openqa.selenium.By;
import org.openqa.selenium.Keys;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;

public class a101TestAutomation {

static WebDriver driver;

    By cerezler = By.xpath("//*[text()='Kabul Et']");
    By giyimAksesuar= By.xpath("(//*[@title='GİYİM & AKSESUAR'])[1]");
    By kadinIcGiyim = By.xpath("//a[@data-value='1565']");
    By dizaltiCorap = By.xpath("//a[@data-value='1567']");
    By ilkCorap = By.xpath("//*[@alt='Penti Kadın 50 Denye Pantolon Çorabı Siyah']");
    By corapRengi = By.xpath("//*[text()='SİYAH']");
    By sepeteEkleButton = By.xpath("//*[@class='add-to-basket button green block with-icon js-add-basket']");
    By sepetiGoruntule = By.xpath("(//*[text()='Sepeti Görüntüle'])[2]");
    By sepetiOnaylaButton = By.xpath("//*[@class='button green checkout-button block js-checkout-button']");
    By uyeOlmadanDevamEtButton = By.xpath("//*[@title='ÜYE OLMADAN DEVAM ET']");
    By emailEkrani = By.xpath("//*[@class='page-inner']");
    String email = "HPTesting1@yandex.com";
    By emailEnter = By.xpath("//*[@name='user_email']");
    By adresEkrani = By.xpath("//*[@class='page-checkout js-page-checkout js-tab-box']");
    By adresOlustur = By.xpath("(//*[@class='new-address js-new-address'])[1]");
    By adresBasligi = By.xpath("//*[@placeholder='Ev adresim, iş adresim vb.']");
    By musteriAdi = By.xpath("//*[@name='first_name']");
    By musteriSoyadi = By.xpath("//*[@name='last_name']");
    By musteriTelefonNumarasi = By.xpath("//*[@name='phone_number']");
    By musteriIl = By.xpath("//*[@name='city']");
    By musteriIlce = By.xpath("//*[@name='township']");
    By musteriMahalle = By.xpath("//*[@class='js-district']");
    By musteriAdres = By.xpath("//*[@name='line']");
    By kaydetButton = By.xpath("//*[@class='button green js-set-country js-prevent-emoji']");
    By kaydetVeDevamEtButton = By.xpath("//button[@class='button block green js-proceed-button']");
    By siparisiTamamlaButton = By.xpath("//*[@class=\"order-complete\"]");
    By odemeEkrani = By.xpath("//*[@class='page-checkout js-page-checkout js-tab-box']");
    
    
    
    public static void setUp(){
        WebDriverManager.chromedriver().setup();
        driver = new ChromeDriver();
        driver.manage().window().maximize();
        driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(15));
        System.out.println("Proje başarılı!");
    }
    
    
    public void test() throws InterruptedException {


        //"https://www.a101.com.tr/" url açılır
        driver.get("https://www.a101.com.tr/");
        System.out.println("A101 sayfasi açıldı.");

        //Çerazleri kabul et butonu tıklanır
        driver.findElement(cerezler).click();
        System.out.println("Cerezler kabul edildi.");


        //Giyim & Aksesuar tıklanır
        driver.findElement(giyimAksesuar).click();
        System.out.println("Giyim ve aksesuar kategorisi secildi.");

        //Kategorilerden kadın içgiyim seçilir
        driver.findElement(kadinIcGiyim).click();
        System.out.println("Kategorilerden icgiyim secildi");

        //Alt menüden kadın dizaltı çorap seçilir
        driver.findElement(dizaltiCorap).click();
        System.out.println("Alt menüden kadın dizaltı çorap secildi.");

        //İlk çıkan çoraba tıklanılır
        driver.findElement(ilkCorap).click();
        System.out.println("Ilk cikan corap secildi.");

        //Siyah olduğu doğrulanır
        Assert.assertTrue(driver.findElement(corapRengi).isDisplayed());
        System.out.println("Secilen corabin siyah oldugu dogrulandi.");


        //Sayfa yenilenir
        //driver.navigate().refresh();


        //Sepete ekle butonu tıklanır
        driver.findElement(sepeteEkleButton).click();
        System.out.println("Sepete ekle butonu tiklandi");

        //Sepeti görüntüle butonu tıklanır
        driver.findElement(sepetiGoruntule).click();
        System.out.println("Sepeti goruntule butonu tiklandi");

        //Sepeti onayla butonu tıklanır
        driver.findElement(sepetiOnaylaButton).click();
        System.out.println("Sepeti onayla butonu tiklandi");


        //Üye olmadan devam et butonu tıklanır
        driver.findElement(uyeOlmadanDevamEtButton).click();
        System.out.println("Uye olmadan devam et butonu tiklandi");


        //E-Mail ekranı gelir.
        Assert.assertTrue(driver.findElement(emailEkrani).isDisplayed());
        System.out.println("E-Mail ekraninin geldigi dogrulanir");

        //Bir mail adresi girilir.
        driver.findElement(emailEnter).sendKeys(email, Keys.ENTER);
        System.out.println("E-Mail adresi girilir");


        //Adres ekranı gelir.
        Assert.assertTrue(driver.findElement(adresEkrani).isDisplayed());
        System.out.println("Adres ekraninin geldigi dogrulanir");


        //Adres oluştur seçeneğine tıklanır
        driver.findElement(adresOlustur).click();
        System.out.println("Adres olustur secenegi tiklanir");

        //Adres ekleme kısımları doldurulur
        //Adres Başlığı
        driver.findElement(adresBasligi).sendKeys("Ev Adresi");

        //Ad
        driver.findElement(musteriAdi).sendKeys("Sanal");

        //Soyad
        driver.findElement(musteriSoyadi).sendKeys("MÜŞTERİ");

        //Telefon
        driver.findElement(musteriTelefonNumarasi).sendKeys("1234567891");

        //İl seçiniz
        driver.findElement(musteriIl).sendKeys("Ankara");
        Thread.sleep(1000);

        //İlçe seçiniz
        driver.findElement(musteriIlce).sendKeys("Çankaya");
        Thread.sleep(1000);

        //Mahalle seçiniz
        driver.findElement(musteriMahalle).sendKeys("Bahçelievler Mah");
        Thread.sleep(1000);

        //Adresinizi yazınız
        driver.findElement(musteriAdres).sendKeys("Bahçelievler Mahallesi 100.Yıl Sokak Yıldırım Sitesi A2 Blok Çankaya/ANKARA");
        Thread.sleep(2000);

        //Kaydet butonuna tıklanır
        driver.findElement(kaydetButton).sendKeys(Keys.ENTER);
        System.out.println("Kaydet butonuna basilir");
        Thread.sleep(2000);

        //Kaydet ve devam et butonu tıklanır
        driver.findElement(kaydetVeDevamEtButton).click();
        System.out.println("Kaydet ve devam et butonuna tiklanir.");
        Thread.sleep(1000);

        //Siparişi tamamla butonu tıklanır
        driver.findElement(siparisiTamamlaButton).click();
        System.out.println("Siparişi tamamla butonu tıklanır.");

        //Ödeme ekranına gelindiği doğrulanır
        Assert.assertTrue(driver.findElement(odemeEkrani).isDisplayed());
        System.out.println("Odeme ekranina gelindigi dogrulanir.");
    }

    @AfterClass
    public static void tearDown(){
        driver.quit();
    }

}
