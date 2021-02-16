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
ms.openlocfilehash: e318d7a709a09e67ebf423db0263985523d2fc28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406805"
---
# <a name="createiprop"></a>CreateIProp

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um objeto de dados de propriedade, ou seja, [um objeto IPropData.](ipropdataimapiprop.md) 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
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
  
> [in] Ponteiro para um IID (identificador de interface) para o objeto de dados de propriedade. O identificador de interface válido é IID_IMAPIPropData. Passar NULL no parâmetro  _lpInterface_ também faz com que o objeto de dados de propriedade retornado no parâmetro  _lppPropData_ seja cast para a interface padrão de um objeto de dados de propriedade. 
    
 _lpAllocateBuffer_
  
> [in] Ponteiro para a [função MAPIAllocateBuffer,](mapiallocatebuffer.md) a ser usado para alocar memória. 
    
 _lpAllocateMore_
  
> [in] Ponteiro para a [função MAPIAllocateMore,](mapiallocatemore.md) a ser usado para alocar memória adicional. 
    
 _lpFreeBuffer_
  
> [in] Ponteiro para a [função MAPIFreeBuffer,](mapifreebuffer.md) a ser usado para liberar memória. 
    
 _lpvReserved_
  
> [in] Reservado; deve ser zero. 
    
 _lppPropData_
  
> [out] Ponteiro para um ponteiro para o objeto de dados de propriedade retornado.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Não há suporte para a interface solicitada para esse objeto.
    
## <a name="remarks"></a>Comentários

Os parâmetros de entrada  _lpAllocateBuffer_,  _lpAllocateMore_ e  _lpFreeBuffer_ apontam para as funções [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)e [MAPIFreeBuffer,](mapifreebuffer.md) respectivamente. Um aplicativo cliente que **chama CreateIProp** passa ponteiros para as funções MAPI nomeadas; um provedor de serviços passa os ponteiros para essas funções recebidas em sua chamada de inicialização ou recuperada com uma chamada para o método [IMAPISupport::GetMemAllocRoutines.](imapisupport-getmemallocroutines.md) 
  

