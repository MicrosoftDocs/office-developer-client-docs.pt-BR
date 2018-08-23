---
title: ScCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyProps
api_type:
- COM
ms.assetid: 08bc256c-9706-4f3e-9a12-3e9cca5e4caa
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: eb3b3b3c9c2e9cffb77febf9c96baed40ce3f9e8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566219"
---
# <a name="sccopyprops"></a>ScCopyProps

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
As propriedades definidas por uma matriz de estruturas de [SPropValue](spropvalue.md) para um novo destino de cópias. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
SCODE ScCopyProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parâmetros

 _cprop_
  
> [in] Contagem de propriedades a serem copiados. 
    
 _rgprop_
  
> [in] Ponteiro para uma matriz de estruturas de [SPropValue](spropvalue.md) que definem as propriedades a serem copiados. O parâmetro _rgprop_ não tem que apontar para o início da matriz, mas ele deve apontar para o início de uma das estruturas **SPropValue** na matriz. 
    
 _pvDst_
  
> [in] Ponteiro para a posição inicial em memória ao qual esta função copia as propriedades. 
    
 _PCB_
  
> [out] Ponteiro opcional para o tamanho, em bytes, do bloco de memória apontado pelo parâmetro _pvDst_ . 
    
## <a name="return-value"></a>Valor retornado

S_OK
  
> Propriedades foram copiadas com êxito.
    
MAPI_E_INVALID_PARAMETER
  
> Um tipo de propriedade desconhecido foi encontrado.
    
## <a name="remarks"></a>Comentários

A nova matriz e seus dados residem em um buffer criado com uma alocação simples e a função [ScRelocProps](screlocprops.md) pode ser usada para ajustar os ponteiros nas estruturas [SPropValue](spropvalue.md) individuais. Antes desse ajuste, os ponteiros são válidos. 
  
 **ScCopyProps** mantém a ordem da propriedade original para a matriz de propriedade copiados. 
  
O parâmetro _pcb_ é opcional. Se não for nula, ela é definida como o número de bytes armazenado no parâmetro _pvDst_ . 
  
## <a name="see-also"></a>Confira também



[ScDupPropset](scduppropset.md)

