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
ms.openlocfilehash: 635525a1c2c3234d724534d225eb07022afc9956
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592119"
---
# <a name="propcopymore"></a>PropCopyMore

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Copia um valor de propriedade exclusivo de um local de origem para um local de destino. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
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
  
> [out] Ponteiro para o local em que essa função grava uma estrutura de [SPropValue](spropvalue.md) definindo o valor da propriedade copiada. 
    
 _lpSPropValueSrc_
  
> [in] Ponteiro para a estrutura de [SPropValue](spropvalue.md) que contém o valor da propriedade a ser copiado. 
    
 _lpfAllocMore_
  
> [in] Ponteiro para a função [MAPIAllocateMore](mapiallocatemore.md) a ser usado para alocar memória adicional, se o local de destino não é grande o suficiente para armazenar a propriedade a ser copiado. 
    
 _lpvObject_
  
> [in] Ponteiro para um objeto para o qual **MAPIAllocateMore** alocará espaço se necessário. 
    
## <a name="return-value"></a>Valor retornado

S_OK
  
> O valor da propriedade único foi copiado com êxito.
    
MAPI_E_NO_SUPPORT
  
> Um tipo de propriedade desconhecido foi encontrado.
    
## <a name="remarks"></a>Comentários

Um provedor de serviço ou um aplicativo cliente pode usar a função **PropCopyMore** para copiar uma propriedade de uma tabela que está prestes a ser liberado para usá-lo em outros lugares. 
  
 **PropCopyMore** não precisa alocar memória, a menos que o valor da propriedade copiado é de um tipo, como PT_STRING8, que não se encaixam em uma estrutura [SPropValue](spropvalue.md) . Para essas propriedades grandes, a função aloca memória usando a função [MAPIAllocateMore](mapiallocatemore.md) para o qual um ponteiro é passado no parâmetro _lpfAllocMore_ . 
  
Injudicious uso de memória de fragmentos **PropCopyMore** ; Considere usar a função [ScCopyProps](sccopyprops.md) . 
  

