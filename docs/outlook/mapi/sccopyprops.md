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
ms.openlocfilehash: 1afd922459be2ec4bbbd27a61fdf6fcb425548c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411005"
---
# <a name="sccopyprops"></a>ScCopyProps

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Copia as propriedades definidas por uma matriz de [estruturas SPropValue](spropvalue.md) para um novo destino. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
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
  
> [in] Contagem de propriedades a serem copiadas. 
    
 _rgprop_
  
> [in] Ponteiro para uma matriz de [estruturas SPropValue](spropvalue.md) que definem as propriedades a serem copiadas. O  _parâmetro rgprop_ não precisa apontar para o início da matriz, mas deve apontar para o início de uma das estruturas **SPropValue** na matriz. 
    
 _pvDst_
  
> [in] Ponteiro para a posição inicial na memória para a qual essa função copia as propriedades. 
    
 _pcb_
  
> [out] Ponteiro opcional para o tamanho, em bytes, do bloco de memória apontado pelo _parâmetro pvDst._ 
    
## <a name="return-value"></a>Valor de retorno

S_OK
  
> As propriedades foram copiadas com êxito.
    
MAPI_E_INVALID_PARAMETER
  
> Um tipo de propriedade desconhecido foi encontrado.
    
## <a name="remarks"></a>Comentários

A nova matriz e seus dados residem em um buffer criado com uma única alocação, e a função [ScRelocProps](screlocprops.md) pode ser usada para ajustar os ponteiros nas estruturas [SPropValue](spropvalue.md) individuais. Antes desse ajuste, os ponteiros são válidos. 
  
 **ScCopyProps** mantém a ordem de propriedade original para a matriz de propriedades copiada. 
  
O _parâmetro pcb_ é opcional; se não for NULL, será definido como o número de bytes armazenados no _parâmetro pvDst._ 
  
## <a name="see-also"></a>Confira também



[ScDupPropset](scduppropset.md)

