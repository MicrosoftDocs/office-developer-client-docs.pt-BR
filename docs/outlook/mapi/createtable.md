---
title: CreateTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateTable
api_type:
- HeaderDef
ms.assetid: 106ce3d8-d0bf-4a0e-9a15-dc8988d0eb58
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e8c399569e68b8cb55d803733ed93105ea0be799
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435009"
---
# <a name="createtable"></a>CreateTable

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria estruturas e um identificador de objeto para um objeto [ITableData](itabledataiunknown.md) que pode ser usado para criar conteúdo de tabela. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
SCODE CreateTable(
  LPCIID lpInterface,
  ALLOCATEBUFFER FAR * lpAllocateBuffer,
  ALLOCATEMORE FAR * lpAllocateMore,
  FREEBUFFER FAR * lpFreeBuffer,
  LPVOID lpvReserved,
  ULONG ulTableType,
  ULONG ulPropTagIndexColumn,
  LPSPropTagArray lpSPropTagArrayColumns,
  LPTABLEDATA FAR * lppTableData
);
```

## <a name="parameters"></a>Parâmetros

 _lpInterface_
  
> no Ponteiro para um identificador de interface (IID) para o objeto Table Data. O identificador de interface válido é IID_IMAPITableData. Passar NULL no parâmetro _lpInterface_ também faz com que o objeto Table Data retornado no parâmetro _lppTableData_ seja convertido na interface padrão para um objeto Table Data. 
    
 _lpAllocateBuffer_
  
> no Ponteiro para a função [MAPIAllocateBuffer](mapiallocatebuffer.md) , a ser usado para alocar memória. 
    
 _lpAllocateMore_
  
> no Ponteiro para a função [MAPIAllocateMore](mapiallocatemore.md) , a ser usado para alocar memória adicional. 
    
 _lpFreeBuffer_
  
> no Ponteiro para a função [MAPIFreeBuffer](mapifreebuffer.md) , a ser usado para liberar memória. 
    
 _lpvReserved_
  
> no Serve deve ser zero. 
    
 _ulTableType_
  
> no Um tipo de tabela que está disponível para um aplicativo cliente ou provedor de serviços como parte de imApitable [:: GetStatus](imapitable-getstatus.md) retornar dados em seus modos de exibição de tabela. Os valores possíveis são: 
    
TBLTYPE_DYNAMIC 
  
> O conteúdo da tabela é dinâmico e pode ser alterado à medida que os dados subjacentes são alterados. 
    
TBLTYPE_KEYSET 
  
> As linhas da tabela são corrigidas, mas os valores dessas linhas são dinâmicos e podem ser alterados conforme as alterações de dados subjacentes. 
    
TBLTYPE_SNAPSHOT 
  
> A tabela é estática e o conteúdo não é alterado quando os dados subjacentes são alterados. 
    
 _ulPropTagIndexColumn_
  
> no Número de índice da coluna a ser usada ao alterar os dados da tabela. 
    
 _lpSPropTagArrayColumns_
  
> no Ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade que indicam as propriedades necessárias na tabela para a qual o objeto contém dados. 
    
 _lppTableData_
  
> bota Ponteiro para um ponteiro para o objeto de dados da tabela retornado.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

Os parâmetros de entrada _lpAllocateBuffer_, _lpAllocateMore_e _lpFreeBuffer_ apontam para as funções [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)e [MAPIFreeBuffer](mapifreebuffer.md) , respectivamente. Um aplicativo cliente que **** chama CreateTable passa em ponteiros para as funções MAPI apenas nomeadas; um provedor de serviços passa os ponteiros para essas funções recebidas em sua chamada de inicialização ou recuperadas com uma chamada para o método [IMAPISupport:: GetMemAllocRoutines](imapisupport-getmemallocroutines.md) . 
  
## <a name="see-also"></a>Confira também



[IMAPITable : IUnknown](imapitableiunknown.md)

