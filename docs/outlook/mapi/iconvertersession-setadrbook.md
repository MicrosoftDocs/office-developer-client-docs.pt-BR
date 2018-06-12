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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: e6880a32e30b8f208ce5ba0a2d30e635ff464461
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766902"
---
# <a name="iconvertersessionsetadrbook"></a>IConverterSession::SetAdrBook

  
  
**Aplica-se a**: Outlook 
  
Especifica um catálogo de endereços MAPI opcional que usa de MAPI conversor de MIME para resolver endereços ambíguos ao converter uma mensagem MAPI para um fluxo MIME.
  
```cpp
HRESULT IConverterSession::SetAdrBook( 
LPADRBOOK pab); 
```

## <a name="parameters"></a>Par�metros

 _PAB_
  
> [in] Ponteiro para uma [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) interface a ser usado na MAPI para conversão de MIME. Defina esse parâmetro como **null** quando não precisar mais o catálogo de endereços; Isso libera a interface e redefine o conversor para não usar qualquer catálogo de endereços. 
    
## <a name="return-value"></a>Valor retornado

S_OK
  
> A chamada de função é bem-sucedida.
    
## <a name="remarks"></a>Coment�rios

Convertendo um MAPI mensagem para o fluxo de MIME geralmente não exige o registro em log em um perfil MAPI. Entretanto, a especificação de um catálogo de endereços MAPI para conversão requer logon a um perfil para obter o catálogo de endereços.
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI usa MimeToMAPI para converter um arquivo EML em uma mensagem MAPI.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI usa MAPIToMIMEStm para converter uma mensagem MAPI em um arquivo EML.  <br/> |
   
## <a name="see-also"></a>Confira também



[IConverterSession: IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

