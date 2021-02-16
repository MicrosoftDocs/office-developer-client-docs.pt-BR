---
title: PropCopyMore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PropCopyMore
api_type:
- HeaderDef
ms.assetid: 133d47cf-3592-44f3-8cdd-be402d160ee4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 827cdb919499a068f7932d8f1f7ec264ddc5b47c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404467"
---
# <a name="propcopymore"></a>PropCopyMore

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Copia um único valor de propriedade de um local de origem para um local de destino. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
SCODE PropCopyMore(
  LPSPropValue lpSPropValueDest,
  LPSPropValue lpSPropValueSrc,
  ALLOCATEMORE * lpfAllocMore,
  LPVOID lpvObject
);
```

## <a name="parameters"></a>Parâmetros

 _lpSPropValueDest_
  
> [out] Ponteiro para o local no qual essa função grava uma [estrutura SPropValue](spropvalue.md) definindo o valor da propriedade copiada. 
    
 _lpSPropValueSrc_
  
> [in] Ponteiro para a [estrutura SPropValue](spropvalue.md) que contém o valor da propriedade a ser copiada. 
    
 _lpfAllocMore_
  
> [in] Ponteiro para a [função MAPIAllocateMore](mapiallocatemore.md) a ser usada para alocar memória adicional se o local de destino não for grande o suficiente para manter a propriedade a ser copiada. 
    
 _lpvObject_
  
> [in] Ponteiro para um objeto para o qual **MAPIAllocateMore** alocará espaço, se necessário. 
    
## <a name="return-value"></a>Valor de retorno

S_OK
  
> O valor da propriedade única foi copiado com êxito.
    
MAPI_E_NO_SUPPORT
  
> Um tipo de propriedade desconhecido foi encontrado.
    
## <a name="remarks"></a>Comentários

Um aplicativo cliente ou provedor de serviços pode usar a função **PropCopyMore** para copiar uma propriedade de uma tabela que está prestes a ser liberada para usá-la em outro lugar. 
  
 **PropCopyMore** não precisa alocar memória, a menos que o valor da propriedade copiada seja de um tipo, como PT_STRING8, que não se encaixe em uma [estrutura SPropValue.](spropvalue.md) Para essas propriedades grandes, a função aloca memória usando a função [MAPIAllocateMore](mapiallocatemore.md) para a qual um ponteiro é passado no parâmetro _lpfAllocMore._ 
  
Uso incondicioso da memória de fragmentos **propCopyMore;** considere usar a [função ScCopyProps.](sccopyprops.md) 
  

