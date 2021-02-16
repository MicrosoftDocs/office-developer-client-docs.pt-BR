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
ms.openlocfilehash: 50fd96acd0989459c9887770ec5a3a236f182da5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418369"
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
  
> [in] O número da linha para a qual as propriedades de retorno são retornadas. O valor no parâmetro  _ulRowNumber_ pode ser qualquer valor de 0, que indica a primeira linha na tabela, até n - 1, que indica a última linha na tabela. 
    
 _lppSRow_
  
> [out] Um ponteiro para um ponteiro para uma [estrutura SRow](srow.md) que descreve a linha de destino. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A linha foi recuperada com êxito ou não existe uma linha para o número de linha especificado pelo _parâmetro ulRowNumber._ 
    
## <a name="remarks"></a>Comentários

O **método ITableData::HrEnumRow** recupera uma linha com base em um número sequencial. Esse número representa a ordem de inserção (0 indica a primeira linha e o número de linhas menos 1 indica a última linha). O MAPI mantém essa ordem cronológica de inserção de linha durante o tempo de vida do objeto de dados da tabela. 
  
Se o número especificado em  _ulRowNumber_ não corresponder a uma linha na tabela, **HrEnumRow** retornará S_OK e define o parâmetro  _lppSRow_ como NULL. 
  
MAPI aloca memória para a estrutura **SRow** retornada usando a função [MAPIAllocateBuffer](mapiallocatebuffer.md) quando o objeto de dados de tabela é criado. O chamador deve liberar essa memória chamando a [função MAPIFreeBuffer.](mapifreebuffer.md) 
  
Para recuperar linhas de uma tabela na ordem em que foram inseridas, os usuários do objeto de dados de tabela chamam o **método HrEnumRow.** 
  
## <a name="see-also"></a>Confira também



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SRow](srow.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

