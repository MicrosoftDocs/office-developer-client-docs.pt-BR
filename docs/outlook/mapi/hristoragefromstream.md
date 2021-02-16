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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416829"
---
# <a name="hristoragefromstream"></a>HrIStorageFromStream

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Camada uma **interface IStorage** em um **objeto IStream.** 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
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
  
> [in] Ponteiro para o **objeto IUnknown** implementando **IStream**. 
    
 _lpInterface_
  
> [in] Ponteiro para o identificador de interface (IID) do objeto stream. Qualquer um dos seguintes valores pode ser passado no parâmetro  _lpInterface:_ NULL, IID_IStream ou IID_ILockBytes. Passar NULL em  _lpInterface_ é o mesmo que passar IID_IStream. 
    
 _ulFlags_
  
> [in] Bitmask de sinalizadores que controla como o objeto de armazenamento deve ser criado em relação ao fluxo. A configuração padrão é STGSTRM_RESET, que dá ao objeto de armazenamento acesso somente leitura e o inicia na posição zero do fluxo. Os sinalizadores a seguir podem ser definidos em qualquer combinação, exceto conforme anotou:
    
STGSTRM_CREATE 
  
> Cria um novo objeto de armazenamento para o objeto stream. Esse sinalizador não pode ser definido se o STGSTRM_RESET sinalizador estiver definido. 
    
STGSTRM_CURRENT 
  
> Inicia o armazenamento na posição atual do fluxo. Esse sinalizador não pode ser definido se o STGSTRM_RESET sinalizador estiver definido. 
    
STGSTRM_MODIFY 
  
> Permite que o provedor de serviços de chamada escreva no armazenamento retornado. Esse sinalizador não pode ser definido se o STGSTRM_RESET sinalizador estiver definido. 
    
STGSTRM_RESET 
  
> Inicia o armazenamento na posição zero. Esse sinalizador não pode ser definido se qualquer outro sinalizador estiver definido. 
    
 _lppStorageOut_
  
> [out] Ponteiro para um ponteiro para o objeto **IStorage** retornado. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

Provedores de armazenamento de mensagens **suportam a função HrIStorageFromStream** usando a interface **IStorage** para anexos. Os provedores da Loja devem implementar a interface **IStream.** **HrIStorageFromStream** fornece a interface **IStorage** para o **objeto IStream.** É possível passar uma interface **ILockBytes** ou **IStream** em  _lpUnkIn_. 
  

