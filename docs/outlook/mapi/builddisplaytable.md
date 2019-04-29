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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8c5e6078be05ff846b7737ff53e9a6338fcb2141
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431593"
---
# <a name="builddisplaytable"></a>BuildDisplayTable

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria uma tabela de exibição a partir dos dados da página de propriedades contidos em uma ou mais estruturas [DTPAGE](dtpage.md) . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Provedores de serviços  <br/> |
   
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

## <a name="parameters"></a>Parâmetros

 _lpAllocateBuffer_
  
> no Ponteiro para a função [MAPIAllocateBuffer](mapiallocatebuffer.md) , a ser usado para alocar memória. 
    
 _lpAllocateMore_
  
> no Ponteiro para a função [MAPIAllocateMore](mapiallocatemore.md) , a ser usado para alocar memória adicional. 
    
 _lpFreeBuffer_
  
> no Ponteiro para a função [MAPIFreeBuffer](mapifreebuffer.md) , a ser usado para liberar memória. 
    
 _lpMalloc_
  
> Não usados deve ser definido como nulo. 
    
 _hInstance_
  
> no Uma instância de um objeto MAPI do qual o **BuildDisplayTable** recupera recursos. 
    
 _cPages_
  
> no Contagem de estruturas [DTPAGE](dtpage.md) na matriz apontada pelo parâmetro _lpPage_ . 
    
 _lpPage_
  
> no Ponteiro para uma matriz de estruturas **DTPAGE** que contêm informações sobre as páginas da tabela de exibição a serem criadas. 
    
 _ulFlags_
  
> no Bitmask de sinalizadores. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres passadas estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI. 
    
 _lppTable_
  
> bota Ponteiro para um ponteiro para a tabela de exibição, que expõe [](imapitableiunknown.md) a interface IMAPITable. 
    
 _lppTblData_
  
> [in, out] Ponteiro para um ponteiro para um objeto Table Data expondo a interface [ITableData](itabledataiunknown.md) na tabela retornada no parâmetro _lppTable_ . Se nenhum objeto de dados de tabela for desejado, _lppTblData_ deve ser definido como nulo em vez de um valor de ponteiro. 
    
## <a name="return-value"></a>Valor de retorno

Nenhum
  
## <a name="remarks"></a>Comentários

MAPI usa as funções apontadas por _lpAllocateBuffer_, _lpAllocateMore_e _lpFreeBuffer_ para a maioria da alocação de memória e desalocação, em particular para alocar memória para uso por aplicativos cliente ao chamar interfaces de objeto como [IMAPIProp::](imapiprop-getprops.md) GetProps e IMAPITable [:: QueryRows](imapitable-queryrows.md). 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Tudo o que é possível é ler do recurso de caixa de diálogo, incluindo:
  
- O título da página ou seja, o membro _ulbLpszLabel_ da estrutura [DTBLPAGE](dtblpage.md) lida do título da caixa de diálogo no recurso. 
    
- Todos os títulos de controle ou seja, os membros _ulbLpszLabel_ de outras estruturas de controle lêem do texto de controle no recurso. 
    
 **BuildDisplayTable** substitui qualquer coisa que tenha passado nas estruturas de controle de entrada com informações do recurso de caixa de diálogo, o que significa que o chamador do **BuildDisplayTable** não pode especificar dinamicamente títulos de página ou de controle. Os chamadores que precisam fazer isso podem fazer com que o **BuildDisplayTable** retorne o objeto de dados de tabela no _lppTableData_ e altere as linhas nele; ou podem criar a tabela de exibição manualmente em um objeto Table Data. 
  
Se _lppTableData_ não estiver definido como NULL, o provedor será responsável por liberar o objeto Table Data quando ele for concluído com a tabela de exibição. 
  

