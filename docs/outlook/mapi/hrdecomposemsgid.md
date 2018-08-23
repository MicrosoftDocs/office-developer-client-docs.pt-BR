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
ms.openlocfilehash: 828d7ebcbceead02441165e3af92ec7b47d9f001
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564623"
---
# <a name="hrdecomposemsgid"></a>HrDecomposeMsgID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Separa a representação ASCII do identificador de entrada compostos de um objeto, geralmente em uma mensagem em um armazenamento de mensagens para o identificador de entrada desse objeto no repositório e o identificador de entrada da loja. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Aplicativos cliente  <br/> |
   
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
  
> [in] A cadeia de caracteres representando o identificador de entrada do objeto. 
    
 _pcbStoreEID_
  
> [out] Ponteiro para o tamanho retornado, em bytes, do identificador de entrada do repositório de mensagem que contém o objeto. Se o parâmetro _szMsgID_ aponta para um identificador de entrada noncompound cadeia de caracteres, em seguida, os pontos de parâmetro _pcbStoreEID_ como zero. 
    
 _ppStoreEID_
  
> [out] Ponteiro para um ponteiro para o identificador retornado de entrada do repositório de mensagem que contém o objeto. Se o parâmetro _szMsgID_ aponta para um identificador de entrada noncompound, NULL é retornado no parâmetro _ppStoreEID_ . 
    
 _pcbMsgEID_
  
> [out] Ponteiro para o tamanho retornado, em bytes, do identificador de entrada do objeto dentro de seu armazenamento. Se o parâmetro _szMsgID_ aponta para uma cadeia de caracteres do identificador de entrada noncompound, o parâmetro _pcbMsgEID_ é igual ao valor do parâmetro _cbEID_ . 
    
 _ppMsgEID_
  
> [out] Ponteiro para um ponteiro para a cadeia de caracteres de identificador retornado de entrada do objeto dentro de seu armazenamento. Se o parâmetro _szMsgID_ aponta para um identificador de entrada noncompound, _ppMsgEID_ aponta para um ponteiro para uma cópia convertida do identificador de entrada noncompound. 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

Se o identificador especificado pelo parâmetro _szMsgID_ for composto, ele é convertido de ASCII e dividido o identificador de entrada do objeto dentro de seu armazenamento de mensagens e o identificador de entrada da loja. Cadeias de caracteres de identificador de entrada noncompound simplesmente são convertidas e copiadas. A cadeia de caracteres de identificador compostos sejam separados é geralmente uma criada pela função [HrComposeMsgID](hrcomposemsgid.md) . 
  
Chamar a função **HrDecomposeMsgID** é equivalente a chamar a função [HrEntryIDFromSz](hrentryidfromsz.md) e, em seguida, a função [HrDecomposeEID](hrdecomposeeid.md) . 
  

