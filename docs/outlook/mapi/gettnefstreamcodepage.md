---
title: GetTnefStreamCodepage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f22ccf2-1004-4731-9d68-f66c01b4588b
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: c4859fa4f8f55af7913c884e25c96727c063ba79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766657"
---
# <a name="gettnefstreamcodepage"></a>GetTnefStreamCodepage

  
  
**Aplica-se a**: Outlook 
  
Determina a página de código para um fluxo de Transport-Neutral Encapsulation Format (TNEF).
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |TNEF.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente.  <br/> |
   
```cpp
HRESULT GetTnefStreamCodepage(
  LPSTREAM lpStream,
  ULONG FAR * lpulCodepage,
  ULONG FAR * lpulSubCodepage
);
```

## <a name="parameters"></a>Par�metros

 _lpStream_
  
> [in] Ponteiro para um armazenamento stream objeto OLE **IStream** interface, fornecendo uma fonte para uma mensagem de fluxo TNEF. 
    
 _lpulCodepage_
  
> [out] Ponteiro para a página de código do fluxo.
    
 _lpulSubCodepage_
  
> [out] Ponteiro para a página subcódigo do fluxo.
    
## <a name="return-value"></a>Valor retornado

 **S_OK**
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
 **MAPI_E_NOT_ENOUGH_DISK**
  
> Houve um erro ao ler um atributo no stream TNEF.
    
 **MAPI_E_CORRUPT_DATA**
  
> O fluxo não era um stream TNEF ou houve um erro ao ler o atributo attOemCodepage.
    
## <a name="remarks"></a>Coment�rios

Use a função **GetTnefStreamCodepage** para ler o atributo **attOemCodepage** do stream TNEF para determinar a página de código e a página subcódigo. Se **attOemCodepage** não for encontrado, **GetTnefStreamCodepage** retorna uma página de código dos 437 e uma página de subcódigo 0. 
  
## <a name="see-also"></a>Confira também



[attOemCodepage](http://msdn.microsoft.com/en-us/library/ee158667%28EXCHG.80%29.aspx)

