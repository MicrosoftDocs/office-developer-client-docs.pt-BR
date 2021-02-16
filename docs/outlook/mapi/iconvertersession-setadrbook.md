---
title: IConverterSessionSetAdrBook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetAdrBook
api_type:
- COM
ms.assetid: d276ab19-17f4-01c7-4b44-b578e631b5fe
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7645208e6a0256957deb3a71ba3e04ad125a6b61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429191"
---
# <a name="iconvertersessionsetadrbook"></a>IConverterSession::SetAdrBook

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica um Address Book MAPI opcional que o conversor MAPI para MIME usa para resolver endereços ambíguos ao converter uma mensagem MAPI em um fluxo MIME.
  
```cpp
HRESULT IConverterSession::SetAdrBook( 
LPADRBOOK pab); 
```

## <a name="parameters"></a>Parâmetros

 _pab_
  
> [in] Ponteiro para um [IAddrBook : interface IMAPIProp](iaddrbookimapiprop.md) a ser usada na conversão MAPI para MIME. De definir esse parâmetro como **nulo** quando você não precisar mais do Address Book; isso libera a interface e redefine o conversor para não usar o Address Book. 
    
## <a name="return-value"></a>Valor de retorno

S_OK
  
> A chamada de função é bem-sucedida.
    
## <a name="remarks"></a>Comentários

A conversão de uma mensagem MAPI em fluxo MIME geralmente não requer logor em um perfil MAPI. No entanto, a especificação de um Address Book MAPI para conversão requer o registro em um perfil para obter o Address Book.
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI usa MimeToMAPI para converter um arquivo EML em uma mensagem MAPI.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI usa MAPIToMIMEStm para converter uma mensagem MAPI em um arquivo EML.  <br/> |
   
## <a name="see-also"></a>Confira também



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

