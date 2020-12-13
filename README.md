using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class yonetici : MonoBehaviour
{
    public  int i;
    float zaman_a = 0.5f;
    float kalan_z = 0.0f;
    public GameObject elma;
    // Start is called before the first frame update
    void Start()
    {
        
        //Invoke("saniye_azalt", 1.0f);  // burada saniye azalt fonksiyonunu 1 sn sonra calistiracak
        //InvokeRepeating("saniye_azalt", 0.0f, 1.0f); // burada baslayacagi zamani belirliyoruz  diger parametre kac sn sonra tekrarlanacagini
        InvokeRepeating("elma_ekle", 0.0f, 0.3f);
    }

  /*  void saniye_azalt()
    {
        saniye--;
        Debug.Log(saniye.ToString());
        if (saniye == 5)
        {
            CancelInvoke("saniye_azalt");// burada calisan fonksiyonu kapatabiliyoruz eger icine fonkston ismi yazmazsan butun invoke fonksyonlarini durdurur
        }

    }
*/
  void elma_ekle()
    {

        float rast = Random.Range(2f, 10f); // burda random sayilar uretiyor 
        GameObject yeni_elma = Instantiate(elma, new Vector3(rast, 10, -9), Quaternion.identity); // yine burada carpisma kontrol ediliyor
    }


    void Update()
    {
      //  Debug.Log(Time.time);   // burada  oyun icerisinde gecen  saniyeyi ogreniyoruz

       // Time.timeScale=0.5f;   // burada ise oyun ici zamani belirledigimiz olcude yavaslatiyoruz
            
    }
}
