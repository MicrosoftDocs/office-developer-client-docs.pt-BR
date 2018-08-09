---
title: ITableDataHrQueryRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrQueryRow
api_type:
- COM
ms.assetid: 66ce8f36-2b2b-4a8e-b9b2-43782d8357a1
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 92540159386e6f37d93684aff037b235071010f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767723"
---
# <a name="itabledatahrqueryrow"></a>ITableData::HrQueryRow

  
  
**Aplica-se a**: Outlook 
  
Recupera uma linha da tabela.
  
```cpp
HRESULT HrQueryRow(
  LPSPropValue lpSPropValue,
  LPSRow FAR * lppSRow,
  ULONG FAR * lpuliRow
);
```

## <a name="parameters"></a>Parâmetros

 _lpSPropValue_
  
> [in] Um ponteiro para uma estrutura de valor de propriedade que descreve a coluna de índice da linha a ser recuperada. O membro **ulPropTag** da estrutura de valor de propriedade deve conter a mesma marca de propriedade, como o parâmetro _ulPropTagIndexColumn_ da chamada para a função de [CreateTable](createtable.md) , que acessa a implementação de [ITableData](itabledataiunknown.md) . 
    
 _lppSRow_
  
> [out] Um ponteiro para um ponteiro para a linha recuperada. 
    
 _lpuliRow_
  
> [além, out] Na entrada, um ponteiro válido ou NULL, que indica que nenhuma informação precisa ser retornado. Na saída, um ponteiro válido que aponta para o número da linha da linha, um número sequencial que identifica a posição da linha na tabela.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A linha foi recuperada com êxito.
    
MAPI_E_INVALID_PARAMETER 
  
> O [SPropValue](spropvalue.md) estruturar que aponta de _lpSPropValue_ para não contém a propriedade de coluna de índice. 
    
## <a name="remarks"></a>Comentários

O método **ITableData::HrQueryRow** recupera todas as propriedades para a linha que tem uma coluna de índice que corresponde ao valor da coluna de índice incluída na estrutura de propriedade apontada pela _lpSPropValue_. **HrQueryRow** também retorna o número da linha, se o chamador solicita-lo, que identifica a posição da linha na tabela. 
  
Porque **HrQueryRow** não modifica a estrutura **SPropValue** apontada pela _lpSPropValue_, os chamadores devem liberar a estrutura quando **HrQueryRow** retorna. Os chamadores também devem liberar a estrutura **SRow** que contém a linha recuperada. 
  
## <a name="see-also"></a>Confira também



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropValue](spropvalue.md)
  
[SRow](srow.md)
  
[ITableData : IUnknown](itabledataiunknown.md)
