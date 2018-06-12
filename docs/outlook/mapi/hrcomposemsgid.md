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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 418ffdd19412dcf948d36a5e7df33f7978d0df3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766768"
---
# <a name="hrcomposemsgid"></a>HrComposeMsgID

  
  
**Aplica-se a**: Outlook 
  
Cria uma cadeia de caracteres ASCII que representa um identificador de compostos de entrada para um objeto, geralmente em uma mensagem em um armazenamento de mensagens. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Aplicativos cliente  <br/> |
   
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

## <a name="parameters"></a>Par�metros

 _psession_
  
> [in] Ponteiro para a sessão em uso pelo aplicativo cliente. 
    
 _cbStoreRecordKey_
  
> [in] Tamanho, em bytes, da chave do registro do repositório de mensagem que contém a mensagem ou outro objeto. Se o parâmetro _cbStoreRecordKey_ é passado zero, os pontos de parâmetro _pszMsgID_ para uma cópia do identificador de entrada é convertido em texto. 
    
 _pStoreRecordKey_
  
> [in] Ponteiro para a chave de registro do repositório de mensagem que contém a mensagem ou outro objeto. 
    
 _cbMsgEID_
  
> [in] Tamanho, em bytes, do identificador de entrada de mensagem ou outro objeto. 
    
 _pMsgEID_
  
> [in] Ponteiro para o identificador de entrada do objeto. 
    
 _pszMsgID_
  
> [out] Ponteiro para a cadeia de caracteres ASCII retornado. Se o parâmetro _cbStoreRecordKey_ for maior do que zero, os pontos de parâmetro _pszMsgID_ a um identificador de entrada compostos convertidos em texto. Se _cbStoreRecordKey_ for zero, _pszMsgID_ pontos a um identificador de entrada noncompound é convertido em texto. 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

Se a mensagem ou outro objeto para o qual está sendo criado o identificador de entrada compostos residir em um armazenamento de mensagens, a sequência identifier é criada do identificador de entrada do objeto e a chave do registro da loja. Se o objeto não estiver em um repositório, ou seja, se o número de bytes para a chave de registro do repositório passado no parâmetro _cbStoreRecordKey_ for zero, o identificador de entrada do objeto é simplesmente copiado e convertido em uma cadeia de caracteres. 
  
Chamar a função **HrComposeMsgID** é equivalente a chamar a função [HrComposeEID](hrcomposeeid.md) e, em seguida, a função [HrSzFromEntryID](hrszfromentryid.md) . 
  
 **HrComposeMsgID** permite que os aplicativos de cliente trabalhar com objetos em repositórios de vários devido ao uso de identificadores de entrada compostos. Um aplicativo pode chamar a função [HrDecomposeMsgID](hrdecomposemsgid.md) para dividir o identificador de entrada compostos em seus constituintes originais. 
  

