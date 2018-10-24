---
title: ITableDataHrEnumRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrEnumRow
api_type:
- COM
ms.assetid: b25d9f2b-9454-4983-98f7-6a051a3b8a04
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 140efe0b2d1b428a94b5bb2919d461779613932a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564679"
---
# <a name="itabledatahrenumrow"></a>ITableData::HrEnumRow

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Recupera uma linha com base em sua posição na tabela. 
  
```cpp
HRESULT HrEnumRow(
  ULONG ulRowNumber,
  LPSRow FAR * lppSRow
);
```

## <a name="parameters"></a>Parâmetros

 _ulRowNumber_
  
> [in] O número da linha para o qual retornar propriedades. O valor no parâmetro _ulRowNumber_ pode ser qualquer valor de 0, que indica a primeira linha na tabela, por meio de n - 1, que indica a última linha da tabela. 
    
 _lppSRow_
  
> [out] Um ponteiro para um ponteiro para uma estrutura de [SRow](srow.md) que descreve a linha de destino. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A linha foi recuperada com êxito, ou uma linha para o número da linha especificada pelo parâmetro _ulRowNumber_ não existe. 
    
## <a name="remarks"></a>Comentários

O método **ITableData::HrEnumRow** recupera uma linha com base em um número sequencial. Este número representa a ordem de inserção (0 indica que a primeira linha e o número de linhas menos 1 indica a última linha). MAPI mantém nesta ordem cronológica de inserção de linha para o tempo de vida do objeto de dados de tabela. 
  
Se o número especificado na _ulRowNumber_ não corresponde a uma linha na tabela, **HrEnumRow** Retorna S_OK e define o parâmetro _lppSRow_ como NULL. 
  
MAPI aloca memória para a estrutura de **SRow** retornada usando a função [MAPIAllocateBuffer](mapiallocatebuffer.md) quando o objeto de dados de tabela é criado. O chamador deve liberar essa memória chamando a função [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Para recuperar linhas de uma tabela na ordem em que foram inseridos, os usuários de objeto de dados de tabela chame o método de **HrEnumRow** . 
  
## <a name="see-also"></a>Confira também



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SRow](srow.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

