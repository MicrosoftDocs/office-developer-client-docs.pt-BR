---
title: Integração com o Office de aplicativos do Android
manager: soliver
ms.date: 06/18/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: a765fa49-a272-4047-9147-59cc68e5dd27
description: Office para Android fornece uma solução extensível que permite a integração com aplicativos de terceiros. É possível integrar com o Office a partir de seu aplicativo Android passando-se os usuários de seu aplicativo para o Office.
ms.openlocfilehash: 2fd60c7e86d3390bc5343f3e09fb2235f97e0b13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765722"
---
# <a name="integrate-with-office-from-android-applications"></a>Integração com o Office de aplicativos do Android

Office para Android fornece uma solução extensível que permite a integração com aplicativos de terceiros. É possível integrar com o Office a partir de seu aplicativo Android passando-se os usuários de seu aplicativo para o Office.
  
Você pode permitir que os usuários que estiverem executando o Office em um dispositivo Android para abrir e editar arquivos armazenados no SharePoint ou OneDrive de qualquer aplicativo. Para fazer isso, você passa arquivos para o Office via manipuladores de protocolo e você se certificar de que o Office é invocado de forma que o Office pode entender.
  
Quando um usuário é feito editando um arquivo, eles podem escolher a chave voltar no dispositivo para voltar para o aplicativo de armazenamento original.
  
## <a name="verify-that-office-has-been-installed"></a>Verificar se o Office foi instalado

Seu aplicativo referência primeiro precisará verificar se um aplicativo específico do Office está instalado. Os seguintes aplicativos do Office podem ser instalados em dispositivos Android para exibição e edição de documentos: 
  
- Excel
    
- PowerPoint
    
- Word
    
Use o Android PackageManager para determinar se um aplicativo específico do Office está instalado no dispositivo. A tabela a seguir lista os nomes de pacote para os aplicativos do Office que você pode usar nesse processo.
  
|**Application**|**Nome do pacote**|
|:-----|:-----|
|Excel  <br/> |com.microsoft.Office.Excel  <br/> |
|PowerPoint  <br/> |com.microsoft.Office.PowerPoint  <br/> |
|Word  <br/> |com.microsoft.Office.Word  <br/> |
   
### <a name="prompt-the-user-to-install-office"></a>Solicita ao usuário para instalar o Office

Se um aplicativo específico do Office não estiver instalado, você pode solicitar o usuário para instalar o aplicativo. A tabela a seguir lista os locais de instalação disponíveis para aplicativos do Office.
  
|**Application**|**Repositório de tocar do Google**|
|:-----|:-----|
|Excel  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.excel](https://play.google.com/store/apps/details?id=com.microsoft.office.excel) <br/> |
|PowerPoint  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.powerpoint](https://play.google.com/store/apps/details?id=com.microsoft.office.powerpoint) <br/> |
|Word  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.word](https://play.google.com/store/apps/details?id=com.microsoft.office.word) <br/> |
   
## <a name="invoke-office"></a>Invocar o Office

Quando o aplicativo do Office for instalado, o seu aplicativo referência pode chamar Office passando-se os seguintes detalhes:
  
- Protocolo do Office
    
- Modo de abertura
    
- URL
    
Formato de esquema:
  
 `<Office protocol><open mode>|u|<URL>`
  
O exemplo a seguir mostra uma solicitação para chamar um arquivo do Word para edição.
  
 `ms-word:ofe|u|https://contoso/Q4/budget.docx`
  
### <a name="office-protocols"></a>Protocolos do Office

A tabela a seguir lista os protocolos para cada aplicativo do Office.
  
|**Application**|**Protocolo**|
|:-----|:-----|
|Excel  <br/> |MS excel:  <br/> |
|PowerPoint  <br/> |MS-powerpoint:  <br/> |
|Word  <br/> |MS-word:  <br/> |
   
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
  
## <a name="see-also"></a>Confira também
<a name="bk_addresources"> </a>

- [Integração com o Office](integrate-with-office.md)
    
- [PackageManager](http://developer.android.com/reference/android/content/pm/PackageManager.html)
    
- [GetPackageManager()](http://developer.android.com/reference/android/content/Context.html)
    

