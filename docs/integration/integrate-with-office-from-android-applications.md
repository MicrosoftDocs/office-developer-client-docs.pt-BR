---
title: Integração com o Office em aplicativos do Android
manager: soliver
ms.date: 06/18/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: a765fa49-a272-4047-9147-59cc68e5dd27
description: Office para Android oferece uma solução extensiva que permite a integração com aplicativos de terceiros. É possível integrar com o Office a partir do seu aplicativo de Android passando usuários de seu aplicativo do Office.
ms.openlocfilehash: 4e674b3d66f3acba7e9c9c19e716ff0d73d803b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303147"
---
# <a name="integrate-with-office-from-android-applications"></a>Integração com o Office em aplicativos do Android

Office para Android oferece uma solução extensiva que permite a integração com aplicativos de terceiros. É possível integrar com o Office a partir do seu aplicativo de Android passando usuários de seu aplicativo do Office.
  
Você pode habilitar os usuários que estão executando o Office em um dispositivo Android para abrir e editar arquivos armazenados no SharePoint ou no OneDrive de qualquer aplicativo. Para fazer isso, você passa arquivos para o Office por meio de identificadores de protocolo e garante que o Office será invocado de uma maneira que Office possa entender.
  
Quando um usuário concluir a edição de um arquivo, ele pode  escolher a tecla voltar no dispositivo para retornar ao aplicativo de armazenamento original.
  
## <a name="verify-that-office-has-been-installed"></a>Verifique se o Office foi instalado

O aplicativo de referência primeiramente precisará verificar se um aplicativo específico do Office está instalado. Os seguintes aplicativos do Office podem ser instalados em dispositivos Android para documento visualização e edição: 
  
- Excel
    
- PowerPoint
    
- Word
    
Use o PackageManager Android para determinar se um aplicativo específico do Office está instalado no dispositivo. A tabela a seguir lista os nomes de pacote para os aplicativos do Office que você pode usar no processo.
  
|**Aplicativo**|**Nome do pacote**|
|:-----|:-----|
|Excel  <br/> |com.microsoft.Office.Excel  <br/> |
|PowerPoint  <br/> |com.microsoft.Office.PowerPoint  <br/> |
|Word  <br/> |com.microsoft.Office.Word  <br/> |
   
### <a name="prompt-the-user-to-install-office"></a>Solicitar que o usuário instale o Office

Se um aplicativo específico do Office não estiver instalado, poderá solicitar ao usuário que instale o aplicativo. A tabela a seguir lista os locais disponíveis para instalação de aplicativos do Office.
  
|**Aplicativo**|**Google Play Store**|
|:-----|:-----|
|Excel  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.excel](https://play.google.com/store/apps/details?id=com.microsoft.office.excel) <br/> |
|PowerPoint  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.powerpoint](https://play.google.com/store/apps/details?id=com.microsoft.office.powerpoint) <br/> |
|Word  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.word](https://play.google.com/store/apps/details?id=com.microsoft.office.word) <br/> |
   
## <a name="invoke-office"></a>Usar o Office

Quando o aplicativo do Office estiver instalado, o aplicativo de referência poderá invocar Office passando os seguintes detalhes:
  
- Protocolo do Office
    
- Modo de abertura
    
- URL
    
Formato de esquema:
  
 `<Office protocol><open mode>|u|<URL>`
  
O exemplo a seguir mostra uma solicitação para invocar um arquivo do Word para edição.
  
 `ms-word:ofe|u|https://contoso/Q4/budget.docx`
  
### <a name="office-protocols"></a>Protocolos do Office

A tabela a seguir lista os protocolos de cada aplicativo do Office.
  
|**Aplicativo**|**Protocolo**|
|:-----|:-----|
|Excel  <br/> |ms-excel:  <br/> |
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
  
## <a name="see-also"></a>Confira também
<a name="bk_addresources"> </a>

- [Integração com o Office](integrate-with-office.md)
    
- [PackageManager](https://developer.android.com/reference/android/content/pm/PackageManager.html)
    
- [GetPackageManager()](https://developer.android.com/reference/android/content/Context.html)
    

