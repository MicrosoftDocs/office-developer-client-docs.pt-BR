---
title: ScRelocProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScRelocProps
api_type:
- COM
ms.assetid: 4aafb254-6074-4a7c-b915-d3d33304ac38
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c73fb96c9620a90ab0505b394fcb9853d02dcde5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421085"
---
# <a name="screlocprops"></a>ScRelocProps

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Ajusta os ponteiros em uma [matriz SPropValue](spropvalue.md) depois que a matriz e seus dados foram copiados ou movidos para um novo local. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
SCODE ScRelocProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parâmetros

 _cprop_
  
> [in] Contagem de propriedades na matriz apontada pelo _parâmetro rgprop._ 
    
 _rgprop_
  
> [in] Ponteiro para uma matriz de [estruturas SPropValue](spropvalue.md) para as quais ponteiros devem ser ajustados. 
    
 _pvBaseOld_
  
> [in] Ponteiro para o endereço base original da matriz apontado pelo _parâmetro rgprop._ 
    
 _pvBaseNew_
  
> [in] Ponteiro para o novo endereço base da matriz apontado pelo _parâmetro rgprop._ 
    
 _pcb_
  
> [in, out] Ponteiro opcional para o tamanho, em bytes, da matriz indicada pelo _parâmetro pvBaseNew._ Se não for NULL, o _parâmetro pcb_ será definido como o número de bytes armazenados no _parâmetro pvD._ 
    
## <a name="return-value"></a>Valor de retorno

S_OK
  
> Os ponteiros foram ajustados com êxito.
    
MAPI_E_INVALID_PARAMETER
  
> Um ou ambos os parâmetros eram inválidos ou um tipo de propriedade desconhecido foi encontrado.
    
## <a name="remarks"></a>Comentários

A **função ScRelocProps** opera na suposição de que a matriz de valores de propriedade para a qual os ponteiros são ajustados foi originalmente alocada em uma única chamada semelhante a uma chamada para a **função ScCopyProps.** Se um aplicativo cliente ou provedor de serviços estiver trabalhando com um valor de propriedade criado a partir de blocos de memória não adjacentes, ele deverá usar [ScCopyProps](sccopyprops.md) para copiar propriedades em vez disso. 
  
 **ScRelocProps** é usado para manter a validade de ponteiros em uma [matriz SPropValue.](spropvalue.md) Para manter a validade dos ponteiros ao escrever essa matriz e lê-la a partir de um disco, execute as seguintes operações: 
  
1. Antes de escrever a matriz e os dados em um disco, chame **ScRelocProps** na matriz com o parâmetro  _pvBaseNew_ apontando para algum valor padrão zero, por exemplo. 
    
2. Depois de ler a matriz e os dados de um disco, chame **ScRelocProps** na matriz com o parâmetro  _pvBaseOld_ igual ao mesmo valor padrão usado na Etapa 1. A matriz e os dados devem ser lidos em um buffer criado com uma única alocação. 
    
3. O  _parâmetro pcb_ para **ScRelocProps** é opcional. 
    
## <a name="see-also"></a>Confira também



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ScCountProps](sccountprops.md)
  
[ScDupPropset](scduppropset.md)
  
[ScRelocNotifications](screlocnotifications.md)

