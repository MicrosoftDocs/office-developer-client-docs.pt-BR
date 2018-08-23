---
title: CreateIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CreateIProp
api_type:
- COM
ms.assetid: 9bf68814-2564-433d-b762-3d2c83ca3c60
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8d6eb011e65ad44f4183eb5821697dcf2508032c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566877"
---
# <a name="createiprop"></a>CreateIProp

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um objeto de dados de propriedade, ou seja, um objeto [IPropData](ipropdataimapiprop.md) . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
SCODE CreateIProp(
  LPCIID lpInterface,
  ALLOCATEBUFFER FAR * lpAllocateBuffer,
  ALLOCATEMORE FAR * lpAllocateMore,
  FREEBUFFER FAR * lpFreeBuffer,
  LPVOID lpvReserved,
  LPPROPDATA FAR * lppPropData
);
```

## <a name="parameters"></a>Parâmetros

 _lpInterface_
  
> [in] Ponteiro para um identificador de interface (IID) para o objeto de dados de propriedade. O identificador de interface válido é IID_IMAPIPropData. Passar NULL no parâmetro _lpInterface_ também fará com que o objeto de dados de propriedade retornado no parâmetro _lppPropData_ para ser convertido para a interface padrão para um objeto de dados de propriedade. 
    
 _lpAllocateBuffer_
  
> [in] Ponteiro para a função de [MAPIAllocateBuffer](mapiallocatebuffer.md) , para ser usado para alocar memória. 
    
 _lpAllocateMore_
  
> [in] Ponteiro para a função de [MAPIAllocateMore](mapiallocatemore.md) , para ser usado para alocar memória adicional. 
    
 _lpFreeBuffer_
  
> [in] Ponteiro para a função [MAPIFreeBuffer](mapifreebuffer.md) , que será usada para liberar memória. 
    
 _lpvReserved_
  
> [in] Reservado; deve ser zero. 
    
 _lppPropData_
  
> [out] Ponteiro para um ponteiro para o objeto de dados de propriedade retornados.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> A interface solicitada não é suportada para este objeto.
    
## <a name="remarks"></a>Comentários

Os parâmetros de entrada _lpAllocateBuffer_, _lpAllocateMore_e _lpFreeBuffer_ apontam para o [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)e funções [MAPIFreeBuffer](mapifreebuffer.md) , respectivamente. Passa de um aplicativo cliente chamar **CreateIProp** em ponteiros para as funções MAPI apenas nomeadas; um provedor de serviços passa os ponteiros para essas funções ele recebidas em sua chamada de inicialização ou recuperadas com uma chamada ao método [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) . 
  

