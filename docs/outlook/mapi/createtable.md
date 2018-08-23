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
ms.openlocfilehash: 5d4717dad51e7e6b90da59d285268761eec84d7b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564147"
---
# <a name="createtable"></a>CreateTable

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um identificador de objeto para um objeto [ITableData](itabledataiunknown.md) que pode ser usado para criar o conteúdo da tabela e de estruturas. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
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
  
> [in] Ponteiro para um identificador de interface (IID) para o objeto de dados de tabela. O identificador de interface válido é IID_IMAPITableData. Passar NULL no parâmetro _lpInterface_ também fará com que o objeto de dados de tabela retornado no parâmetro _lppTableData_ para ser convertido para a interface padrão para um objeto de dados de tabela. 
    
 _lpAllocateBuffer_
  
> [in] Ponteiro para a função de [MAPIAllocateBuffer](mapiallocatebuffer.md) , para ser usado para alocar memória. 
    
 _lpAllocateMore_
  
> [in] Ponteiro para a função de [MAPIAllocateMore](mapiallocatemore.md) , para ser usado para alocar memória adicional. 
    
 _lpFreeBuffer_
  
> [in] Ponteiro para a função [MAPIFreeBuffer](mapifreebuffer.md) , que será usada para liberar memória. 
    
 _lpvReserved_
  
> [in] Reservado; deve ser zero. 
    
 _ulTableType_
  
> [in] Um tipo de tabela que está disponível para um aplicativo cliente ou de um provedor de serviços como parte dos dados retorno [IMAPITable::GetStatus](imapitable-getstatus.md) em seus modos de exibição de tabela. Os valores possíveis são: 
    
TBLTYPE_DYNAMIC 
  
> O conteúdo da tabela é dinâmico e pode alterar como as alterações de dados subjacente. 
    
TBLTYPE_KEYSET 
  
> As linhas da tabela são corrigidas, mas os valores nessas linhas são dinâmicos e podem alterar como as alterações de dados subjacente. 
    
TBLTYPE_SNAPSHOT 
  
> A tabela é estática e o conteúdo não é alterados quando os dados subjacentes forem alterados. 
    
 _ulPropTagIndexColumn_
  
> [in] Número de índice da coluna para uso ao alterar os dados da tabela. 
    
 _lpSPropTagArrayColumns_
  
> [in] Ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade indicando as propriedades necessárias na tabela para o qual o objeto contém dados. 
    
 _lppTableData_
  
> [out] Ponteiro para um ponteiro para o objeto de dados de tabela retornada.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

Os parâmetros de entrada _lpAllocateBuffer_, _lpAllocateMore_e _lpFreeBuffer_ apontam para o [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)e funções [MAPIFreeBuffer](mapifreebuffer.md) , respectivamente. Um aplicativo cliente chamar **CreateTable** passa em ponteiros para as funções MAPI apenas nomeadas; um provedor de serviços passa os ponteiros para essas funções que ele recebidas em sua chamada de inicialização ou recuperadas com uma chamada ao método [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) . 
  
## <a name="see-also"></a>Confira também



[IMAPITable : IUnknown](imapitableiunknown.md)

