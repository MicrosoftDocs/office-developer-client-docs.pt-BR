---
title: Integração do Office com aplicativos do iOS
manager: soliver
ms.date: 06/04/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: f3a277ba-7ba1-4eea-83b5-915b409f3093
description: O Office para iOS oferece uma solução extensível que permite a integração com aplicativos de terceiros. Este artigo descreve como você pode fazer a integração com o Office a partir do seu aplicativo iOS, passando usuários do seu aplicativo para o Office e, em seguida, retornando-os ao seu aplicativo.
ms.openlocfilehash: d17a096c17eadab0cd94ee1dce18e979e80fa65d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413847"
---
# <a name="integrate-with-office-from-ios-applications"></a>Integração do Office com aplicativos do iOS

O Office para iOS oferece uma solução extensível que permite a integração com aplicativos de terceiros. Este artigo descreve como você pode fazer a integração com o Office a partir do seu aplicativo iOS, passando usuários do seu aplicativo para o Office e, em seguida, retornando-os ao seu aplicativo.
  
Você pode habilitar os usuários que estão executando o Office em um dispositivo iOS para abrir e editar arquivos armazenados no SharePoint ou no OneDrive de qualquer aplicativo e, em seguida, retorná-los rapidamente ao aplicativo original quando eles terminaram de editar o arquivo. Para fazer isso, você passa arquivos para o Office por meio de identificadores de protocolo e garante que o Office será invocado de uma maneira que Office possa entender.
  
Quando um usuário termina de editar um arquivo, ele pode escolher a seta para trás no aplicativo do Office para fechar o documento e retornar ao aplicativo de armazenamento original, desde que você passe informações específicas para o aplicativo do Office quando ele é iniciado.
  
## <a name="verify-that-office-has-been-installed"></a>Verifique se o Office foi instalado

O aplicativo de referência primeiramente precisará verificar se um aplicativo específico do Office está instalado. Os seguintes aplicativos do Office podem ser instalados em dispositivos iOS para visualização e edição de documentos:
  
- Excel
    
- OneNote
    
- PowerPoint
    
- Word
    
Use o método [canOpenURL](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html) para determinar se o aplicativo pode abrir o recurso. Este método obtém a URL do recurso como um parâmetro e retorna **não** se o aplicativo que aceita a URL não está disponível. Se **CanOpenURL** **não**retornar, você precisará solicitar que o usuário instale o Office.
  
### <a name="prompt-the-user-to-install-office"></a>Solicitar que o usuário instale o Office

 Se um determinado aplicativo do Office não estiver instalado, você poderá usar um objeto [SKProductViewController](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html) para renderizar a iTunes App Store em seu aplicativo e mostrar ao usuário o aplicativo do Office a ser instalado. A tabela a seguir lista o identificador iTunes a ser usado para invocar cada aplicativo do Office no controlador de exibição de produto do kit de armazenamento. 
  
|**Aplicativo do Office**|**identificador iTunes**|
|:-----|:-----|
|Excel  <br/> |[https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp; UO = 4](https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp;uo=4) <br/> |
|OneNote (iPhone)  <br/> |[https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp; UO = 4](https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp;uo=4) <br/> |
|PowerPoint  <br/> |[https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp; UO = 4](https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp;uo=4) <br/> |
|Word  <br/> |[https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp; UO = 4](https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp;uo=4) <br/> |
   
## <a name="invoke-office"></a>Usar o Office

Quando o aplicativo do Office estiver instalado, o aplicativo de referência poderá invocar Office passando os seguintes detalhes: 
  
- Protocolo do Office
    
- Modo de abertura
    
- URL
    
- Protocolo passback
    
- Contexto do documento
    
Formato de esquema:
  
 `<Office protocol><open mode>|u|<URL>|p|<passback protocol>|c|<document context>`
  
O exemplo a seguir mostra uma solicitação para invocar um arquivo do Word para edição:
  
 `ms-word:ofe|u|https://contoso/Q4/budget.docx|p|clouddrive|c|folderviewQ4`
  
### <a name="office-protocols"></a>Protocolos do Office

A tabela a seguir lista os protocolos de cada aplicativo do Office. 
  
|**Aplicativo**|**Protocolo**|
|:-----|:-----|
|Excel  <br/> |ms-excel:  <br/> |
|OneNote  <br/> |OneNote  <br/> |
|PowerPoint  <br/> |ms-powerpoint:  <br/> |
|Word  <br/> |ms-word:  <br/> |
   
### <a name="open-mode"></a>Modo de abertura

Aplicativos do Office podem abrir arquivos diretamente no modo de exibição (ofv) ou editar o modo (ofe). O modo de edição é o padrão. 
  
Formato de esquema:
  
 `<ofv or ofe>`
  
### <a name="url"></a>URL

A URL inclui três partes: 
  
- A declaração de que o arquivo será aberto para edição (ofe)
    
- Descritor URL (| u |)
    
- A URL
    
A URL deve ser codificadt e deve ser um link direto para o arquivo (não um redirecionamento). Se a URL está em um formato que não dá suporte a Office ou o download falhar o Office não vai retornar o usuário aplicativo solicitado. 
  
Formato de esquema:
  
 `|u|<document URL>`
  
### <a name="passback-protocol-optional"></a>Protocolo passback (opcional)

Se quiser que o Office retorne usuários para seu aplicativo iOS quando eles escolherem a seta para a direita, o aplicativo de invocação precisará usar o protocolo passback, que inclui o descritor ' | p | ' seguido do protocolo de aplicativo (sem dois-pontos). Você precisará garantir que o aplicativo possa lidar corretamente com a resposta do Office.
  
Formato de esquema:
  
 `|p|<passback protocol>`
  
### <a name="document-context-optional"></a>Contexto de documento (opcional)

O Office não usa o contexto do documento, mas o aplicativo de referência pode precisar dele quando o Office passar um usuário de volta. Se quiser que o contexto do documento seja retornado para seu aplicativo, use o descritor ' | c | ' seguido do contexto desejado como uma cadeia de caracteres. O Office não limita o tamanho da cadeia de caracteres, além de todos os limites impostos pelo sistema operacional.
  
Formato de esquema:
  
 `|c|<document context>`
  
## <a name="return-users-to-the-referring-application"></a>Retornar usuários para o aplicativo de referência

Por motivos de segurança, o Office só retornará os usuários para o aplicativo de referência se o arquivo for aberto com êxito. Quando o usuário escolhe a seta para trás, o Office responde ao aplicativo que está chamando com o protocolo passback, o modo de abertura, a URL, o status de upload pendente e o contexto do documento. O status de upload pendente usa o descritor | z | e é sim ou não.
  
Formato de esquema:
  
 `<app protocol>:ofe|u|<URL>|z|<yes or no>|c|<doc context> Example: clouddrive:ofe|u|https://contoso/Q4/budget.docx|z|no|c|folderviewQ4`
  
## <a name="see-also"></a>Confira também
<a name="bk_addresources"> </a>

- [método canOpenURL](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html)
    
- [Classe UIApplication](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html)
    
- [Objeto SKProductViewController](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html)
    

