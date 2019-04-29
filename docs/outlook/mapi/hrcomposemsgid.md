---
title: HrComposeMsgID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrComposeMsgID
api_type:
- COM
ms.assetid: bb76b147-6552-4cc4-920f-699170aea17f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c035780d3d790d94551860a418401e63da1c2151
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424060"
---
# <a name="hrcomposemsgid"></a>HrComposeMsgID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria uma cadeia de caracteres ASCII representando um identificador de entrada composto para um objeto, geralmente uma mensagem em um repositório de mensagens. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente  <br/> |
   
```cpp
HrComposeMsgID(
  LPMAPISESSION psession,
  ULONG cbStoreRecordKey,
  LPBYTE pStoreRecordKey,
  ULONG cbMsgEID,
  LPENTRYID pMsgEID,
  LPSTR FAR * pszMsgID
);
```

## <a name="parameters"></a>Parâmetros

 _psession_
  
> no Ponteiro para a sessão em uso pelo aplicativo cliente. 
    
 _cbStoreRecordKey_
  
> no Tamanho, em bytes, da chave de registro do repositório de mensagens que contém a mensagem ou outro objeto. Se zero for passado no parâmetro _cbStoreRecordKey_ , o parâmetro _pszMsgID_ apontará para uma cópia do identificador de entrada convertido em texto. 
    
 _pStoreRecordKey_
  
> no Ponteiro para a chave de registro do repositório de mensagens que contém a mensagem ou outro objeto. 
    
 _cbMsgEID_
  
> no Tamanho, em bytes, do identificador de entrada da mensagem ou de outro objeto. 
    
 _pMsgEID_
  
> no Ponteiro para o identificador de entrada do objeto. 
    
 _pszMsgID_
  
> bota Ponteiro para a cadeia de caracteres ASCII retornada. Se o parâmetro _cbStoreRecordKey_ for maior que zero, o parâmetro _pszMsgID_ apontará para um identificador de entrada composto convertido em texto. Se _cbStoreRecordKey_ for zero, _pszMsgID_ apontará para um identificador de entrada não composto convertido em texto. 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

Se a mensagem ou outro objeto para o qual o identificador de entrada composta estiver sendo criado residir em um repositório de mensagens, a cadeia de caracteres do identificador será criada a partir do identificador de entrada do objeto e da chave de registro da loja. Se o objeto não estiver em um repositório, ou seja, se a contagem de bytes para a chave do registro de repositório passada no parâmetro _cbStoreRecordKey_ for zero, o identificador de entrada do objeto será simplesmente copiado e convertido em uma cadeia de caracteres. 
  
Chamar a função **HrComposeMsgID** é equivalente a chamar a função [HrComposeEID](hrcomposeeid.md) e, em seguida, a função [HrSzFromEntryID](hrszfromentryid.md) . 
  
 O **HrComposeMsgID** permite que os aplicativos cliente trabalhem com objetos em vários repositórios por meio do uso de identificadores de entrada compostos. Um aplicativo pode chamar a função [HrDecomposeMsgID](hrdecomposemsgid.md) para dividir o identificador de entrada composta em seus constituintes originais. 
  

