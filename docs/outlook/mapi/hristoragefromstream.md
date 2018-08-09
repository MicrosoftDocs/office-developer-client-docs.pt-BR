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
ms.openlocfilehash: bd2d0a662585e8aba91250786f88dd310fe37e32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766802"
---
# <a name="hristoragefromstream"></a>HrIStorageFromStream

  
  
**Aplica-se a**: Outlook 
  
Uma interface **IStorage** em um objeto **IStream** -camadas. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
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
  
> [in] Ponteiro para o objeto **IUnknown** implementando **IStream**. 
    
 _lpInterface_
  
> [in] Ponteiro para o identificador de interface (IID) para o objeto stream. Qualquer um dos seguintes valores podem ser passados no parâmetro _lpInterface_ : NULL, IID_IStream ou IID_ILockBytes. Passar NULL _lpInterface_ é o mesmo que passar IID_IStream. 
    
 _ulFlags_
  
> [in] Bitmask dos sinalizadores que controla como o objeto de armazenamento deve ser criado em relação ao stream. A configuração padrão é STGSTRM_RESET, que fornece o acesso somente leitura do objeto de armazenamento e a inicia em zero da posição do fluxo. Sinalizadores a seguir podem ser definidos em qualquer combinação, exceto conforme observado:
    
STGSTRM_CREATE 
  
> Cria um novo objeto de armazenamento para o objeto stream. Esse sinalizador não pode ser definida se o sinalizador STGSTRM_RESET está definido. 
    
STGSTRM_CURRENT 
  
> Inicia o armazenamento na posição atual do fluxo. Esse sinalizador não pode ser definida se o sinalizador STGSTRM_RESET está definido. 
    
STGSTRM_MODIFY 
  
> Permite que o provedor de serviços de chamada gravar o armazenamento retornado. Esse sinalizador não pode ser definida se o sinalizador STGSTRM_RESET está definido. 
    
STGSTRM_RESET 
  
> Inicia o armazenamento na posição zero. Esse sinalizador não pode ser definida se qualquer outro sinalizador estiver definido. 
    
 _lppStorageOut_
  
> [out] Ponteiro para um ponteiro para o objeto **|** retornado. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

Mensagem armazenar provedores suportam a função **HrIStorageFromStream** usando a interface de **IStorage** para anexos. Provedores de armazenamento devem implementar a interface **IStream** . **HrIStorageFromStream** fornece a interface de **IStorage** para o objeto **IStream** . É possível passar um **ILockBytes** ou uma interface **IStream** em _lpUnkIn_. 
  

