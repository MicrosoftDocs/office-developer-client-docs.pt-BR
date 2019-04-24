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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329005"
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
  
> bota Aponta para o valor de indicador de 32 bits retornado. Este indicador pode ser passado posteriormente em uma chamada para o método imApitable [:: SeekRow](imapitable-seekrow.md) . 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> A operação solicitada não pôde ser concluída.
    
## <a name="remarks"></a>Comentários

O método imApitable **:: CreateBookmark** marca uma posição de tabela criando um valor chamado indicador. Um indicador pode ser usado para retornar à posição identificada pelo indicador. A posição com indicador é associada ao objeto nessa linha na tabela. 
  
Não há suporte para indicadores em tabelas de anexos e implementações de tabelas **** de anexos de MAPI_E_NO_SUPPORT de retorno de CreateBookmark. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Por causa da despesa de memória de manter posições de cursor com indicadores, limite o número de indicadores que você pode criar. Quando chegar a esse número, retorne MAPI_E_UNABLE_TO_COMPLETE de todas as chamadas **** subsequentes para CreateBookmark.
  
Às vezes, um indicador aponta para uma linha que não está mais no modo de exibição de tabela. Se um chamador usar esse indicador, mova o cursor para a próxima linha visível e pare lá. 
  
Quando o chamador tenta usar um indicador que aponta para uma linha não visível porque foi recolhido, retorne MAPI_W_POSITION_CHANGED após mover o indicador. Você pode reposicionar o indicador para a próxima linha visível no momento ou quando o recolhimento ocorre no método setCollapsestate. **** Se você mover o indicador no momento em que a linha estiver recolhida, deverá manter um bit no indicador que indica exatamente quando o indicador foi movido: desde o último uso ou se ele nunca tiver sido usado desde sua criação. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

 **CreateBookmark** aloca memória para o indicador que cria. Libere os recursos para o indicador chamando o método [IMAPITable:: FreeBookmark](imapitable-freebookmark.md) . 
  
## <a name="see-also"></a>Confira também



[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

