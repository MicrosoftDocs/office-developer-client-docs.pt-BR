---
title: HrDecomposeMsgID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDecomposeMsgID
api_type:
- COM
ms.assetid: 5e6a9f3e-79be-4ffd-9d42-3a14cabb1435
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bff73ee5cf02680a2376106e21e0c743b995d336
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404432"
---
# <a name="hrdecomposemsgid"></a>HrDecomposeMsgID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Separa a representação ASCII do identificador de entrada composta de um objeto, geralmente uma mensagem em um armazenamento de mensagens, no identificador de entrada desse objeto no armazenamento e no identificador de entrada do armazenamento. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos do cliente  <br/> |
   
```cpp
HrDecomposeMsgID(
  LPMAPISESSION psession,
  LPSTR szMsgID,
  ULONG FAR * pcbStoreEID,
  LPENTRYID FAR * ppStoreEID,
  ULONG FAR * pcbMsgEID,
  LPENTRYID FAR * ppMsgEID
);
```

## <a name="parameters"></a>Parâmetros

 _psession_
  
> [in] Ponteiro para a sessão em uso pelo aplicativo cliente. 
    
 _szMsgID_
  
> [in] A cadeia de caracteres que representa o identificador de entrada do objeto. 
    
 _pcbStoreEID_
  
> [out] Ponteiro para o tamanho retornado, em bytes, do identificador de entrada do armazenamento de mensagens que contém o objeto. Se o  _parâmetro szMsgID_ aponta para uma cadeia de caracteres do identificador de entrada não encontrado, o parâmetro  _pcbStoreEID_ aponta para zero. 
    
 _ppStoreEID_
  
> [out] Ponteiro para um ponteiro para o identificador de entrada retornado do armazenamento de mensagens que contém o objeto. Se o _parâmetro szMsgID_ aponta para um identificador de entrada não encontrado, NULL é retornado no _parâmetro ppStoreEID._ 
    
 _pcbMsgEID_
  
> [out] Ponteiro para o tamanho retornado, em bytes, do identificador de entrada do objeto dentro de seu armazenamento. Se o parâmetro _szMsgID_ aponta para uma cadeia de caracteres do identificador de entrada não encontrado, o parâmetro _pcbMsgEID_ é igual ao valor do parâmetro _cbEID._ 
    
 _ppMsgEID_
  
> [out] Ponteiro para um ponteiro para a cadeia de caracteres do identificador de entrada retornado do objeto dentro de seu armazenamento. Se o parâmetro  _szMsgID_ aponta para um identificador de entrada não encontrado,  _ppMsgEID_ aponta para um ponteiro para uma cópia convertida do identificador de entrada não encontrado. 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

Se o identificador especificado pelo parâmetro  _szMsgID_ for composto, ele será convertido de ASCII e dividido no identificador de entrada do objeto no armazenamento de mensagens e no identificador de entrada do armazenamento. As cadeias de caracteres do identificador de entrada não-computador são simplesmente convertidas e copiadas. A cadeia de caracteres do identificador composto a ser separada geralmente é aquela criada pela [função HrComposeMsgID.](hrcomposemsgid.md) 
  
Chamar a **função HrDecomposeMsgID** é equivalente a chamar a função [HrEntryIDFromSz](hrentryidfromsz.md) e, em seguida, [a função HrDecomposeEID.](hrdecomposeeid.md) 
  

