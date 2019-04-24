---
title: HrIStorageFromStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrIStorageFromStream
api_type:
- HeaderDef
ms.assetid: 1cdc95b8-a156-4600-9e20-caaa02680e87
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1362b1131d937ef240aa1962db8c1b5116786c67
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347779"
---
# <a name="hristoragefromstream"></a>HrIStorageFromStream

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Camadas uma interface **IStorage** em um objeto **IStream** . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
HRESULT HrIStorageFromStream(
  LPUNKNOWN lpUnkIn,
  PIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a>Parâmetros

 _lpUnkIn_
  
> no Ponteiro para o objeto **IUnknown** que implementa **IStream**. 
    
 _lpInterface_
  
> no Ponteiro para o identificador de interface (IID) do objeto Stream. Qualquer um dos seguintes valores pode ser passado no parâmetro _lpInterface_ : NULL, IID_IStream ou IID_ILockBytes. Passar NULL em _lpInterface_ é o mesmo que passar IID_IStream. 
    
 _ulFlags_
  
> no Bitmask de sinalizadores que controlam como o objeto de armazenamento deve ser criado em relação ao fluxo. A configuração padrão é STGSTRM_RESET, que fornece ao objeto de armazenamento acesso somente leitura e o inicia na posição zero do fluxo. Os seguintes sinalizadores podem ser definidos em qualquer combinação, exceto conforme observado:
    
STGSTRM_CREATE 
  
> Cria um novo objeto de armazenamento para o objeto Stream. Este sinalizador não pode ser definido se o sinalizador STGSTRM_RESET estiver definido. 
    
STGSTRM_CURRENT 
  
> Inicia o armazenamento na posição atual do Stream. Este sinalizador não pode ser definido se o sinalizador STGSTRM_RESET estiver definido. 
    
STGSTRM_MODIFY 
  
> Permite que o provedor de serviços de chamada grave no armazenamento retornado. Este sinalizador não pode ser definido se o sinalizador STGSTRM_RESET estiver definido. 
    
STGSTRM_RESET 
  
> Inicia o armazenamento na posição zero. Este sinalizador não pode ser definido se qualquer outro sinalizador estiver definido. 
    
 _lppStorageOut_
  
> bota Ponteiro para um ponteiro para o objeto **IStorage** retornado. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

Os provedores de repositórios de mensagens dão suporte à função **HrIStorageFromStream** usando a interface **IStorage** para anexos. Os provedores de repositório devem implementar a interface de **IStream** . **HrIStorageFromStream** fornece a interface **IStorage** para o objeto **IStream** . É possível passar uma interface **ILockBytes** ou **IStream** no _lpUnkIn_. 
  

