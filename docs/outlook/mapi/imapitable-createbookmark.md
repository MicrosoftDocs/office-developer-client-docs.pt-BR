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
ms.openlocfilehash: c251dacce0d4e1743a74f1ba45e395b6e1c05064
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408821"
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
  
> [out] Ponteiro para o valor de indicador de 32 bits retornado. Esse indicador pode ser passado posteriormente em uma chamada para o [método IMAPITable::SeekRow.](imapitable-seekrow.md) 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> A operação solicitada não pôde ser concluída.
    
## <a name="remarks"></a>Comentários

O **método IMAPITable::CreateBookmark** marca uma posição de tabela criando um valor chamado indicador. Um indicador pode ser usado para retornar à posição identificada pelo indicador. A posição do indicador está associada ao objeto nessa linha na tabela. 
  
Bookmarks are not supported on attachment tables, and attachment table implementations of **CreateBookmark** return MAPI_E_NO_SUPPORT. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Devido à despesa de memória com a manutenção de posições do cursor com indicadores, limite o número de indicadores que você pode criar. Quando você alcançar esse número, retorne MAPI_E_UNABLE_TO_COMPLETE de todas as chamadas subsequentes para **CreateBookmark**.
  
Às vezes, um indicador aponta para uma linha que não está mais no ponto de vista da tabela. Se um chamador usar esse indicador, mova o cursor para a próxima linha visível e pare lá. 
  
Quando o chamador tentar usar um indicador que está apontando para uma linha nãovisível porque ela foi recolhido, retorne MAPI_W_POSITION_CHANGED depois de mover o indicador. Você pode reposicionar o indicador para a próxima linha visível neste momento ou quando o rebaixamento ocorrer no **método SetCollapseState.** Se você mover o indicador no momento em que a linha estiver recolhido, deverá manter um pouco no indicador que indica exatamente quando o indicador foi movido: desde seu último uso ou se ele nunca foi usado desde sua criação. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

 **CreateBookmark** aloca memória para o indicador que ele cria. Libere os recursos para o indicador chamando o [método IMAPITable::FreeBookmark.](imapitable-freebookmark.md) 
  
## <a name="see-also"></a>Confira também



[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

