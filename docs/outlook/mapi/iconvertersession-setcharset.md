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
ms.openlocfilehash: 14b2904e57852c564395f4b27c9d5270afd1454a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336656"
---
# <a name="iconvertersessionsetcharset"></a>IConverterSession::SetCharSet

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica um conjunto de caracteres opcional que o conversor MAPI para MIME usa ao converter uma mensagem MAPI em um fluxo MIME.
  
```cpp
HRESULT SetCharset( 
     BOOL fApply, 
     HCHARSET hcharset, 
     CSETAPPLYTYPE csetapplytype); 
```

## <a name="parameters"></a>Parâmetros

 _fApply_
  
> no Indica se um determinado conjunto de caracteres deve ser usado para a conversão. Defina esse parâmetro como **true** para aplicar o conjunto de caracteres em conversões subsequentes. Defina esse parâmetro como **false** se não quiser mais aplicar qualquer conjunto de caracteres específico e retornar aos padrões para as mensagens subsequentes. 
    
 _hcharset_
  
> no Um identificador para um conjunto de caracteres conforme definido em MimeOLE. h do Windows Mail. Especifique **NULL** para especificar que você não deseja aplicar qualquer conjunto de caracteres específico. Para valores não **nulos** , use uma função como [MimeOleGetCodePageCharset](https://msdn.microsoft.com/library/ms714746%28VS.85%29.aspx) para obter um identificador para o conjunto de caracteres. 
    
 _csetapplytype_
  
> no Indica como aplicar um conjunto de caracteres para converter uma mensagem, conforme definido no MimeOLE. h do Windows Mail.
    
## <a name="return-value"></a>Valor de retorno

S_OK
  
> A chamada de função foi bem-sucedida.
    
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MapiMime. cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI usa MimeToMAPI para converter um arquivo EML em uma mensagem MAPI.  <br/> |
|MapiMime. cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI usa MAPIToMIMEStm para converter uma mensagem MAPI em um arquivo EML.  <br/> |
   
## <a name="see-also"></a>Confira também



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

