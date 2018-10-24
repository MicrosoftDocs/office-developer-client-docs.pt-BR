---
title: IMAPITableCreateBookmark
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.CreateBookmark
api_type:
- COM
ms.assetid: 320af2ff-c2a5-43b1-b3a1-76cb5ffd6a4f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5e9135a52c15c18b70116aaf52e1ee63af413673
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563846"
---
# <a name="imapitablecreatebookmark"></a>IMAPITable::CreateBookmark

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um indicador na posição atual da tabela.
  
```cpp
HRESULT CreateBookmark(
BOOKMARK FAR * lpbkPosition
);
```

## <a name="parameters"></a>Parâmetros

 _lpbkPosition_
  
> [out] Ponteiro para o valor retornado indicador de 32 bits. Este indicador posteriormente pode ser passado em uma chamada ao método [IMAPITable::SeekRow](imapitable-seekrow.md) . 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> A operação solicitada não pôde ser concluída.
    
## <a name="remarks"></a>Comentários

O método **IMAPITable::CreateBookmark** marca uma posição tabela criando um valor chamado um indicador. Um indicador pode ser usado para retornar à posição identificada pelo indicador. A posição marcado pelo indicador está associada com o objeto nesse objeto row na tabela. 
  
Indicadores não são suportados em tabelas de anexo e implementações de tabela de anexo do **CreateBookmark** retornam MAPI_E_NO_SUPPORT. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Devido a despesa com a memória de manter as posições de cursor com marcadores, limite o número de indicadores que você pode criar. Quando você chegar a esse número, retorne MAPI_E_UNABLE_TO_COMPLETE de todas as chamadas subsequentes aos **CreateBookmark**.
  
Em alguns casos, um indicador aponta para uma linha que não está mais no modo de exibição de tabela. Se um chamador usar tal um indicador, mova o cursor para a próxima linha visível e parar lá. 
  
Quando o chamador tenta usar um indicador que está apontando para uma linha arquvo porque ele ter sido recolhido, retorne MAPI_W_POSITION_CHANGED depois de mover o indicador. Você pode reposicionar o indicador para a próxima linha visível no momento ou quando o recolhimento ocorre no método **SetCollapseState** . Se você mover o indicador no momento em que a linha estiver recolhida, você deverá manter um pouco no indicador que indica exatamente quando o indicador foi movido: desde que use sua última ou se nunca tiver sido usado desde sua criação. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

 **CreateBookmark** aloca memória para o indicador que ele cria. Libere os recursos para o indicador chamando o método [IMAPITable::FreeBookmark](imapitable-freebookmark.md) . 
  
## <a name="see-also"></a>Confira também



[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

