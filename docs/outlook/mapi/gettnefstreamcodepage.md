---
title: GetTnefStreamCodepage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f22ccf2-1004-4731-9d68-f66c01b4588b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1e3d384f35726ff28bb47f3d537c8a7a1dda6dce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299423"
---
# <a name="gettnefstreamcodepage"></a>GetTnefStreamCodepage

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Determina a página de código para um fluxo TNEF (Transport-neutral Encapsulation Format).
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |TNEF. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços.  <br/> |
   
```cpp
HRESULT GetTnefStreamCodepage(
  LPSTREAM lpStream,
  ULONG FAR * lpulCodepage,
  ULONG FAR * lpulSubCodepage
);
```

## <a name="parameters"></a>Parâmetros

 _lpStream_
  
> no Ponteiro para um objeto de fluxo de armazenamento interface **IStream** de OLE, fornecendo uma fonte para uma mensagem de fluxo TNEF. 
    
 _lpulCodepage_
  
> bota Ponteiro para a página de código do Stream.
    
 _lpulSubCodepage_
  
> bota Ponteiro para a página de subcódigo do Stream.
    
## <a name="return-value"></a>Valor de retorno

 **S_OK**
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
 **MAPI_E_NOT_ENOUGH_DISK**
  
> Ocorreu um erro ao ler um atributo no fluxo TNEF.
    
 **MAPI_E_CORRUPT_DATA**
  
> O Stream não era um fluxo TNEF ou houve um erro ao ler o atributo attOemCodepage.
    
## <a name="remarks"></a>Comentários

Use a função **GetTnefStreamCodepage** para ler o atributo **ATTOEMCODEPAGE** do fluxo TNEF para determinar a página de código e a página de subcódigo. Se **attOemCodepage** não for encontrado, **GetTnefStreamCodepage** retornará uma página de código de 437 e uma página de subcódigo 0. 
  
## <a name="see-also"></a>Confira também



[attOemCodepage](https://msdn.microsoft.com/library/ee158667%28EXCHG.80%29.aspx)

