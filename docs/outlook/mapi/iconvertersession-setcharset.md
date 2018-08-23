---
title: IConverterSessionSetCharSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetCharSet
api_type:
- COM
ms.assetid: 25af3683-3a65-2d39-6f6e-76c8d36f866d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 69023d2c13037fb52a4d1dc4f7376efbd839aebc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581696"
---
# <a name="iconvertersessionsetcharset"></a>IConverterSession::SetCharSet

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica que um caractere opcional definir que a MAPI para MIME conversor usar ao converter uma mensagem MAPI para um fluxo MIME.
  
```cpp
HRESULT SetCharset( 
     BOOL fApply, 
     HCHARSET hcharset, 
     CSETAPPLYTYPE csetapplytype); 
```

## <a name="parameters"></a>Parâmetros

 _fApply_
  
> [in] Indica se deve usar um conjunto para a conversão de caracteres específica. Defina esse parâmetro como **true** para aplicar o conjunto de caracteres no conversões subsequentes. Defina esse parâmetro como **false** , se você não deseja mais aplicar qualquer conjunto de caracteres específico e retornar aos padrões para mensagens subsequentes. 
    
 _hcharset_
  
> [in] Um identificador para um caractere definido como definido no mimeole.h do Windows Mail. Especifique **Nulo** para especificar que você não deseja aplicar qualquer conjunto de caracteres específico. Para valores não - **Nulo** , use uma função como [MimeOleGetCodePageCharset](http://msdn.microsoft.com/en-us/library/ms714746%28VS.85%29.aspx) para obter um identificador para o conjunto de caracteres. 
    
 _csetapplytype_
  
> [in] Indica como aplicar um conjunto de caracteres para converter uma mensagem, conforme definido na mimeole.h do Windows Mail.
    
## <a name="return-value"></a>Valor retornado

S_OK
  
> A chamada de função é bem-sucedida.
    
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI usa MimeToMAPI para converter um arquivo EML em uma mensagem MAPI.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI usa MAPIToMIMEStm para converter uma mensagem MAPI em um arquivo EML.  <br/> |
   
## <a name="see-also"></a>Confira também



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

