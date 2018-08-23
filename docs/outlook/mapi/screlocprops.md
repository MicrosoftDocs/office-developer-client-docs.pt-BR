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
ms.openlocfilehash: 241fac608552036e4706956cbe79524aaedacec9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576845"
---
# <a name="screlocprops"></a>ScRelocProps

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Ajusta os ponteiros em uma matriz de [SPropValue](spropvalue.md) depois que a matriz e seus dados foram copiadas ou movidos para um novo local. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
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
  
> [in] Contagem de propriedades na matriz apontado pelo parâmetro _rgprop_ . 
    
 _rgprop_
  
> [in] Ponteiro para uma matriz de estruturas de [SPropValue](spropvalue.md) no qual ponteiros devem ser ajustadas. 
    
 _pvBaseOld_
  
> [in] Ponteiro para o endereço base original da matriz apontado pelo parâmetro _rgprop_ . 
    
 _pvBaseNew_
  
> [in] Ponteiro para o novo endereço base da matriz apontado pelo parâmetro _rgprop_ . 
    
 _PCB_
  
> [além, out] Ponteiro opcional para o tamanho, em bytes, da matriz indicado pelo parâmetro _pvBaseNew_ . Se não for NULL, o parâmetro _pcb_ estiver definido como o número de bytes armazenado no parâmetro _pvD_ . 
    
## <a name="return-value"></a>Valor retornado

S_OK
  
> Ponteiros foram ajustados com êxito.
    
MAPI_E_INVALID_PARAMETER
  
> Um ou ambos os parâmetros eram inválidos ou um tipo de propriedade desconhecido foi encontrado.
    
## <a name="remarks"></a>Comentários

A função **ScRelocProps** opera no pressuposto de que a matriz de valores de propriedade para o qual os ponteiros são ajustados foi originalmente alocado em uma única chamada semelhante a uma chamada para a função **ScCopyProps** . Se um aplicativo cliente ou um provedor de serviço está trabalhando com um valor de propriedade é construído a partir de blocos não contíguos de memória, ele deve usar [ScCopyProps](sccopyprops.md) para copiar as propriedades em vez disso. 
  
 **ScRelocProps** é usado para manter a validade dos ponteiros em uma matriz [SPropValue](spropvalue.md) . Para manter a validade dos ponteiros ao escrever essa matriz para e lê-lo a partir de um disco, execute as seguintes operações: 
  
1. Antes de gravar a matriz e os dados em um disco, chame **ScRelocProps** na matriz com o parâmetro _pvBaseNew_ apontando para algum valor padrão de zero, por exemplo. 
    
2. Após ler a matriz e os dados de um disco, chame **ScRelocProps** a matriz com o parâmetro _pvBaseOld_ igual com o mesmo valor padrão usado na etapa 1. A matriz e os dados devem ser lido em um buffer criado com uma alocação simples. 
    
3. O parâmetro _pcb_ **ScRelocProps** é opcional. 
    
## <a name="see-also"></a>Confira também



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ScCountProps](sccountprops.md)
  
[ScDupPropset](scduppropset.md)
  
[ScRelocNotifications](screlocnotifications.md)

