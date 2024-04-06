# discord-bot
import discord
from discord.ext import commands

intents = discord.Intents.default()
intents.message_content = True

bot = commands.Bot(command_prefix='!', intents=intents)

AntikCag = {
    "Sokrates": "orgulanmamış bir hayatın yaşamaya değmeyeceğini düşünen Sokrates, Yunan felsefesinin kurucularındandır. Ortaya koyduğu düşünceler felsefe tarihinin Sokrates öncesi ve sonrası olarak ayrılmasına neden olmuştur. Ölüme mahkûm edilen büyük filozof arkasında yazılmış bir eser bırakmamış ama öğrencisi Platon tarafından düşünceleri diyaloglar halinde kayıt altına alınmıştır.",
    "Pisagor": "Sayıların babası olarak bilinen filozof, varoluşu matematikle ilişkilendirmiş ve her şeyin matematikle ölçülebileceği düşüncesini ileri sürmüştür. Pisagor önermesinin sahibi olan düşünürün okulunda kullandığı ve herkesin eşit şekilde içecek içmesini sağlayan “Pisagor’un Adalet Kupası” da dünyada ilgi gören buluşlarından biri olmuştur.",
    "Heraklitos": "Hayatı hakkında çok az şey bilinmesine karşılık Efes’te yaşadığı bilgisi şüphesiz bizim için çok değerlidir. Ateş, su, toprak… Heraklitos’a göre insan bu üç madde ve aralarındaki sürekli dönüşümden meydana gelmiştir.",
    "Platon": "Sokrates'in öğrencisi olan Platon, modern felsefeye yön veren İlk Çağ filozoflarından biridir. Devlet adlı kitabında, ülke yönetiminin nasıl olması gerektiğini ayrıntılı bir şekilde ele almıştır. Evreni ''idealar dünyası'' ve ''nesneler dünyası'' olarak ikiye ayırmıştır. İdealizm akımının kurucusudur. Sonraki yıllarda Alman İdealizmi ve Yeni Platonculuk gibi akımların doğmasında etkili olmuştur. Diğer önemli eserleri: Phaidros, Ruh Üzerine, Şölen, Sokrates'in Savunması ve Gorgias."
}

OrtaCag = {
    "Adi Şankara": "Tüm gerçekliğin Brahma dediği tek bir kaynaktan doğduğunu öne sürmüştür. Çokluk ve farklılık olarak görünen evren bir illüzyondan başka bir şey değildir.",
    "İbn Rüşt": "Din vahiy ürünüyken, felsefeyi ise insan aklının ürünü olarak değer gördü, fakat her ikisinin de kaynağının aynı olduğunu savunur.",
    "Gazali": "İslam inanç felsefesi olan Kelâm'ın daha çok akaid kısmına önem vermiş ve akıl yerine sezgiyi ön planda tutmuştur. Mantık ve münazara ilkelerini kullanmıştır. Bununla beraber Kelam ile tatmin olmayan Gazzâlî tasavvufa yönelerek aklın yerine mükaşefeyi koymuştur."
}

YeniCag = {
    "René Descartes": "Diğer bilimler gibi etiğin de kökleri metafizikteydi. Bu şekilde Tanrı'nın varlığını savunur, insanın doğadaki yerini araştırır, zihin-beden ikiliği teorisini formüle eder ve özgür irade'yi savunur.",
    "Immanuel Kant": "Felsefedeki ilk ve temel misyonunun bilimi temellendirmek, daha sonra da ahlakın ve dinin rasyonelliğini savunmak olduğuna inanmıştır. Bu amacı gerçekleştirmek için, hem Descartes'ın rasyonalizminden ve hem de Hume'un empirizminden önemli gördüğü öğeleri alarak, transandantal epistemolojik idealizm diye bilinen kendi bilgi kuramını geliştirmiş, yükselen bilimin felsefi temellerini gösterdikten sonra, özgürlük ve ödev düşüncesine dayanarak Hristiyan ahlakını savunma çabası vermiştir. O, fenomenal gerçeklikle, yani bizim duyular aracılığıyla tecrübe ettiğimiz dünya ile numenal gerçeklik, yani duyusal olmayan ve hakkında bilgi sahibi olunamayacak dünya arasında bir ayrım yapmıştır.",
    "Friedrich Hegel": "Hegel felsefesi her şeyden önce bireylerin kendi kendilerine ilişkin olarak özgür bir bilince ulaştıkları bir insanlık tarihi felsefesidir. Ama bilinç kendi başına özgür değildir; bilincin özgürleşmesi Tinin Fenomenolojisi'nde betimlenen karmaşık bir süreçle gerçekleşir."
}

YakinCag = {
    "Arthur Schopenhauer": "Schopenhauer, Platon'un ve Immanuel Kant'ın etkisinde idealizmin teorisini kendince anladığı boyutunda temsil ederken, bu genel bakışı subjektif idealizmin sınırlarından taşıramamış ve Hegel'in felsefesini de reddetmiştir. ",
    "Friedrich Nietzsche": "Gelenek karşıtlarının kutsalıdır. Ne nihilisttir, ne de irrasyonalist; aksine boş ve irrasyonel dünyanın habercisidir. Benzersiz bir kavrayış gücünün poetik yetiyle kaynaştığı yerde kendini dışavuran bir 'kâhin'. Onun felsefesine genel bir bakış, dehasını teslim etmeyi gerektirir.",
    "William James": "Pratik deneyim ile insan hayatını anlamlandırmayı amaçlayan bir yöntem felsefesi ve bir dünya görüşüdür. James, yaşanılan dünyanın kusurlu olduğunu ve bunun ancak insan eliyle iyileştirilebileceğini iddia eder."
}


@bot.command()
async def cevap(ctx, cag):
    if cag == "AntikCag":
        await ctx.send(str(AntikCag))
    elif cag == "OrtaCag":
        await ctx.send(str(OrtaCag))
    elif cag == "YeniCag":
        await ctx.send(str(YeniCag))
    elif cag == "YakinCag":
        await ctx.send(str(YakinCag))
    else:
        await ctx.send("Geçerli bir çağ seçiniz.")

bot.run(Token_Giriniz)
