---
title: Integração do Office com aplicativos do iOS
manager: soliver
ms.date: 06/04/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: f3a277ba-7ba1-4eea-83b5-915b409f3093
description: Office para iOS fornece uma solução extensível que permite a integração com aplicativos de terceiros. Este artigo descreve como você pode integrar com o Office do seu aplicativo iOS passando os usuários de seu aplicativo para Office, e, em seguida, retornando-los ao seu aplicativo.
ms.openlocfilehash: 2ba8e1a157953705b60ff0cac7d62bafade0c469
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765728"
---
# <a name="integrate-with-office-from-ios-applications"></a>Integração do Office com aplicativos do iOS

Office para iOS fornece uma solução extensível que permite a integração com aplicativos de terceiros. Este artigo descreve como você pode integrar com o Office do seu aplicativo iOS passando os usuários de seu aplicativo para Office, e, em seguida, retornando-los ao seu aplicativo.
  
Você pode permitir que os usuários que estão executando o Office em um dispositivo iOS para abrir e editar arquivos armazenados no SharePoint ou OneDrive de qualquer aplicativo e, em seguida, rapidamente voltar para o aplicativo original quando eles terminar edição do arquivo. Para fazer isso, você passa arquivos para o Office via manipuladores de protocolo e você se certificar de que o Office é invocado de forma que o Office pode entender.
  
Quando um usuário é feito editando um arquivo, eles podem escolher na seta para voltar no aplicativo do Office para fechar o documento e retornar para o aplicativo de armazenamento original, desde que você passa informações específicas para o aplicativo do Office quando ele é iniciado.
  
## <a name="verify-that-office-has-been-installed"></a>Verificar se o Office foi instalado

Seu aplicativo referência primeiro precisará verificar se um aplicativo específico do Office está instalado. Os seguintes aplicativos do Office podem ser instalados nos dispositivos de iOS para exibição e edição de documentos:
  
- Excel
    
- OneNote
    
- PowerPoint
    
- Word
    
Use o método [canOpenURL](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html) para determinar se o seu aplicativo pode abrir o recurso. Esse método leva a URL para o recurso como um parâmetro e retorna **não** se o aplicativo que aceita a URL não estiver disponível. Se **canOpenURL** retornará **não**, você precisará solicitar ao usuário para instalar o Office.
  
### <a name="prompt-the-user-to-install-office"></a>Solicita ao usuário para instalar o Office

 Se um aplicativo específico do Office não estiver instalado, você pode usar um objeto [SKProductViewController](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html) para renderizar iTunes app store em seu aplicativo e mostrar ao usuário o aplicativo do Office para instalar. A tabela a seguir lista o identificador do iTunes usar para invocar a cada aplicativo do Office no controlador de modo de exibição de produto do Kit de repositório. 
  
|**Aplicativo do Office**|**Identificador iTunes**|
|:-----|:-----|
|Excel  <br/> |[https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp; uo = 4](https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp;uo=4) <br/> |
|OneNote (iPad)  <br/> |[https://itunes.apple.com/us/app/microsoft-onenote-for-ipad/id478105721?mt=8&amp; uo = 4](https://itunes.apple.com/us/app/microsoft-onenote-for-ipad/id478105721?mt=8&amp;uo=4) <br/> |
|OneNote (iPhone)  <br/> |[https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp; uo = 4](https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp;uo=4) <br/> |
|PowerPoint  <br/> |[https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp; uo = 4](https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp;uo=4) <br/> |
|Word  <br/> |[https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp; uo = 4](https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp;uo=4) <br/> |
   
## <a name="invoke-office"></a>Invocar o Office

Quando o aplicativo do Office for instalado, o seu aplicativo referência pode chamar Office passando-se os seguintes detalhes: 
  
- Protocolo do Office
    
- Modo de abertura
    
- URL
    
- Protocolo Passback
    
- Contexto de documento
    
Formato de esquema:
  
 `<Office protocol><open mode>|u|<URL>|p|<passback protocol>|c|<document context>`
  
O exemplo a seguir mostra uma solicitação para chamar um arquivo do Word para edição:
  
 `ms-word:ofe|u|https://contoso/Q4/budget.docx|p|clouddrive|c|folderviewQ4`
  
### <a name="office-protocols"></a>Protocolos do Office

A tabela a seguir lista os protocolos para cada aplicativo do Office. 
  
|**Application**|**Protocolo**|
|:-----|:-----|
|Excel  <br/> |ms-excel:  <br/> |
|OneNote  <br/> |OneNote:  <br/> |
|PowerPoint  <br/> |ms-powerpoint:  <br/> |
|Word  <br/> |ms-word:  <br/> |
   
### <a name="open-mode"></a>Modo de abertura

Aplicativos do Office podem abrir arquivos diretamente no modo de exibição (ofv) ou Editar modo (ofe). Modo de edição é o padrão. 
  
Formato de esquema:
  
 `<ofv or ofe>`
  
### <a name="url"></a>URL

A URL inclui três partes: 
  
- A declaração de que o arquivo será aberto para edição (ofe)
    
- O descritor de URL (| u |)
    
- A URL
    
A URL tem que ser codificada e deve ser um link direto para o arquivo (não um redirecionamento). Se a URL estiver em um formato Office não dá suporte ou o download simplesmente falhar, o Office não retornará o usuário ao aplicativo de chamada. 
  
Formato de esquema:
  
 `|u|<document URL>`
  
### <a name="passback-protocol-optional"></a>Protocolo de Passback (opcional)

Se desejar que o Office para retornar usuários ao seu aplicativo iOS quando escolherem na seta para voltar, o aplicativo de invocação precisará usar o protocolo passback, que inclui o descritor ' | p |' seguido pelo protocolo app (sem dois-pontos). Você precisará garantir que o seu aplicativo pode manipular corretamente a resposta do Office.
  
Formato de esquema:
  
 `|p|<passback protocol>`
  
### <a name="document-context-optional"></a>Contexto de documento (opcional)

Office não usa o contexto do documento, mas o aplicativo de referência talvez precisem quando Office passa de volta um usuário. Se desejar que o contexto do documento a ser retornado ao seu aplicativo, use o descritor ' | c |' seguido de contexto que deseja usar como uma cadeia de caracteres. Office não limitam o comprimento da cadeia de caracteres, além de quaisquer limites impostas pelo sistema operacional.
  
Formato de esquema:
  
 `|c|<document context>`
  
## <a name="return-users-to-the-referring-application"></a>Retornar usuários para o aplicativo de referência

Por motivos de segurança, Office retorna apenas os usuários para o aplicativo de referência se o arquivo foi aberto com êxito. Quando o usuário escolhe regressivo seta para baixo, Office responde ao aplicativo de invocação com o protocolo passback, abra o carregamento de modo, URL, status pendente e contexto de documentos. O carregamento de status pendente usa o descritor | z |, e é Sim ou não.
  
Formato de esquema:
  
 `<app protocol>:ofe|u|<URL>|z|<yes or no>|c|<doc context> Example: clouddrive:ofe|u|https://contoso/Q4/budget.docx|z|no|c|folderviewQ4`
  
## <a name="see-also"></a>Confira também
<a name="bk_addresources"> </a>

- [método canOpenURL](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html)
    
- [Classe de UIApplication](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html)
    
- [Objeto SKProductViewController](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html)
    

