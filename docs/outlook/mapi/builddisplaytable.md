---
title: BuildDisplayTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BuildDisplayTable
api_type:
- HeaderDef
ms.assetid: 0846415b-6fe1-4504-8620-108af6719015
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: b821394f32a938f4878ee93e685aafbeb0786597
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766255"
---
# <a name="builddisplaytable"></a>BuildDisplayTable

  
  
**Aplica-se a**: Outlook 
  
Cria uma tabela de exibição dos dados da página de propriedade contidos em uma ou mais estruturas [DTPAGE](dtpage.md) . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços  <br/> |
   
```cpp
STDAPI BuildDisplayTable(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  LPMALLOC lpMalloc,
  HINSTANCE hInstance,
  UINT cPages,
  LPDTPAGE lpPage,
  ULONG ulFlags,
  LPMAPITABLE * lppTable,
  LPTABLEDATA * lppTblData
);
```

## <a name="parameters"></a>Par�metros

 _lpAllocateBuffer_
  
> [in] Ponteiro para a função de [MAPIAllocateBuffer](mapiallocatebuffer.md) , para ser usado para alocar memória. 
    
 _lpAllocateMore_
  
> [in] Ponteiro para a função de [MAPIAllocateMore](mapiallocatemore.md) , para ser usado para alocar memória adicional. 
    
 _lpFreeBuffer_
  
> [in] Ponteiro para a função [MAPIFreeBuffer](mapifreebuffer.md) , que será usada para liberar memória. 
    
 _lpMalloc_
  
> Não utilizado; deve ser definido como NULL. 
    
 _hInstance_
  
> [in] Uma instância de um objeto MAPI do qual **BuildDisplayTable** recupera recursos. 
    
 _cPages_
  
> [in] Contagem de estruturas [DTPAGE](dtpage.md) na matriz apontado pelo parâmetro _lpPage_ . 
    
 _lpPage_
  
> [in] Ponteiro para uma matriz de estruturas **DTPAGE** que contêm informações sobre as páginas de tabela de exibição a ser criado. 
    
 _ulFlags_
  
> [in] Bitmask dos sinalizadores. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres passada na estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI. 
    
 _lppTable_
  
> [out] Ponteiro para um ponteiro para a tabela de exibição, que expõe a interface [IMAPITable](imapitableiunknown.md) . 
    
 _lppTblData_
  
> [além, out] Ponteiro para um ponteiro para um objeto de dados de tabela expondo a interface [ITableData](itabledataiunknown.md) na tabela retornada no parâmetro _lppTable_ . Se nenhum objeto de dados de tabela for desejado, _lppTblData_ deve ser definido como NULL, em vez de um valor de ponteiro. 
    
## <a name="return-value"></a>Valor retornado

None
  
## <a name="remarks"></a>Comentários

O MAPI usa as funções apontadas pela _lpAllocateBuffer_, _lpAllocateMore_e _lpFreeBuffer_ para a maioria dos alocação de memória e desalocação, especificamente para alocar memória para uso por aplicativos do cliente, ao chamar interfaces de objeto como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md). 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Tudo possível é lido a partir do recurso de diálogo, incluindo:
  
- O título da página que é, o membro _ulbLpszLabel_ da estrutura [DTBLPAGE](dtblpage.md) ler o título de diálogo no recurso. 
    
- Todos os títulos de controle que é, os membros _ulbLpszLabel_ outras estruturas de controle ler o texto do controle no recurso. 
    
 **BuildDisplayTable** substitui qualquer coisa passados as estruturas de controle de entrada com as informações do recurso de diálogo, o que significa que o chamador de **BuildDisplayTable** dinamicamente não é possível especificar os títulos de página ou o controle. Chamadores que precisam fazer o que podem ter **BuildDisplayTable** retornam o objeto de dados de tabela em _lppTableData_ e altere linhas nela; ou, eles podem criar a tabela de exibição manualmente em um objeto de dados de tabela, em vez disso. 
  
Se _lppTableData_ não estiver definida como NULL, o provedor é responsável por liberar o objeto de dados de tabela quando ele for concluído com a tabela de exibição. 
  

