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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348087"
---
# <a name="hrdecomposemsgid"></a>HrDecomposeMsgID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Separa a representação ASCII do identificador de entrada composta de um objeto, geralmente uma mensagem em um repositório de mensagens, no identificador de entrada desse objeto no repositório e no identificador de entrada da loja. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente  <br/> |
   
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
  
> no Ponteiro para a sessão em uso pelo aplicativo cliente. 
    
 _szMsgID_
  
> no A cadeia de caracteres que representa o identificador de entrada do objeto. 
    
 _pcbStoreEID_
  
> bota Ponteiro para o tamanho retornado, em bytes, do identificador de entrada do repositório de mensagens que contém o objeto. Se o parâmetro _szMsgID_ apontar para uma cadeia de caracteres de identificador de entrada não composta, o parâmetro _pcbStoreEID_ apontará para zero. 
    
 _ppStoreEID_
  
> bota Ponteiro para um ponteiro para o identificador de entrada retornado do repositório de mensagens que contém o objeto. Se o parâmetro _szMsgID_ apontar para um identificador de entrada não composta, NULL será retornado no parâmetro _ppStoreEID_ . 
    
 _pcbMsgEID_
  
> bota Ponteiro para o tamanho retornado, em bytes, do identificador de entrada do objeto dentro de seu repositório. Se o parâmetro _szMsgID_ apontar para uma cadeia de caracteres de identificador de entrada não composta, o parâmetro _pcbMsgEID_ será igual ao valor do parâmetro _cbEID_ . 
    
 _ppMsgEID_
  
> bota Ponteiro para um ponteiro para a cadeia de caracteres de identificador de entrada retornada do objeto dentro de seu repositório. Se o parâmetro _szMsgID_ apontar para um identificador de entrada não composta, _ppMsgEID_ apontará para um ponteiro para uma cópia convertida do identificador de entrada não composta. 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

Se o identificador especificado pelo parâmetro _szMsgID_ for composto, ele será convertido de ASCII e dividido no identificador de entrada do objeto no repositório de mensagens e no identificador de entrada da loja. Cadeias de caracteres de identificador de entrada não compostos são apenas convertidos e copiados. A cadeia de caracteres de identificador composto a ser separada é normalmente uma criada pela função [HrComposeMsgID](hrcomposemsgid.md) . 
  
Chamar a função **HrDecomposeMsgID** é equivalente a chamar a função [HrEntryIDFromSz](hrentryidfromsz.md) e, em seguida, a função [HrDecomposeEID](hrdecomposeeid.md) . 
  

