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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399652"
---
# <a name="gettnefstreamcodepage"></a>GetTnefStreamCodepage

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Determina a página de código para um fluxo de Transport-Neutral Encapsulation Format (TNEF).
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |TNEF.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Provedores de serviços e aplicativos cliente.  <br/> |
   
```cpp
HRESULT GetTnefStreamCodepage(
  LPSTREAM lpStream,
  ULONG FAR * lpulCodepage,
  ULONG FAR * lpulSubCodepage
);
```

## <a name="parameters"></a>Parâmetros

 _lpStream_
  
> [in] Ponteiro para um armazenamento stream objeto OLE **IStream** interface, fornecendo uma fonte para uma mensagem de fluxo TNEF. 
    
 _lpulCodepage_
  
> [out] Ponteiro para a página de código do fluxo.
    
 _lpulSubCodepage_
  
> [out] Ponteiro para a página subcódigo do fluxo.
    
## <a name="return-value"></a>Valor de retorno

 **S_OK**
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
 **MAPI_E_NOT_ENOUGH_DISK**
  
> Houve um erro ao ler um atributo no stream TNEF.
    
 **MAPI_E_CORRUPT_DATA**
  
> O fluxo não era um stream TNEF ou houve um erro ao ler o atributo attOemCodepage.
    
## <a name="remarks"></a>Comentários

Use a função **GetTnefStreamCodepage** para ler o atributo **attOemCodepage** do stream TNEF para determinar a página de código e a página subcódigo. Se **attOemCodepage** não for encontrado, **GetTnefStreamCodepage** retorna uma página de código dos 437 e uma página de subcódigo 0. 
  
## <a name="see-also"></a>Confira também



[attOemCodepage](https://msdn.microsoft.com/library/ee158667%28EXCHG.80%29.aspx)

