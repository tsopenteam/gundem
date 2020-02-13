# gundem - Teknoseyir Haftalık Gündem Değerlendirmesi

### Haftalık Gündem Değerlendirmesi Nedir ?

> teknoseyir.com tarafından haftalık olarak yapılan, teknoloji ile ilgili konuların konuşulduğu bir programdır.
> Olabildiğince her hafta yayınlanır.

### gundem.json Nedir ?

> Yayınlanan tüm gündem bilgilerinin kayıt altına alındığı proje.

### Kullanım

> gundem.json dosyasında tüm gündemleri bulabilirsiniz.
> İstediğiniz yerde, istediğiniz şekilde kullanabilirsiniz.
> Yeni yayınlanan gündemler json dosyasına eklenmektedir.

### Json Veri Yapısı

```typescript
declare module namespace {

    export interface Content {
        contentText: string;
        contentLink: string[];
    }

    export interface List {
        year: string;
        count: number;
        totalCount: number;
        uploadDate: string;
        podcastLink: string;
        videoLink: string;
        siteLink: string;
        rangeFirstDate: string;
        rangeLastDate: string;
        titlePodcast: string;
        explanationPodcast: string;
        content: Content[];
    }

    export interface RootObject {
        list: List[];
    }

}
```