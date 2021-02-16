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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: da41fadc9a71a410dd115e28ce2cf9c81442b104
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434764"
---
# <a name="itabledatahrqueryrow"></a>ITableData::HrQueryRow

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Recupera uma linha de tabela.
  
```cpp
HRESULT HrQueryRow(
  LPSPropValue lpSPropValue,
  LPSRow FAR * lppSRow,
  ULONG FAR * lpuliRow
);
```

## <a name="parameters"></a>Parâmetros

 _lpSPropValue_
  
> [in] Um ponteiro para uma estrutura de valores de propriedade que descreve a coluna de índice para a linha a ser recuperada. O **membro ulPropTag** da estrutura de valores de propriedade deve conter a mesma marca de propriedade que o parâmetro _ulPropTagIndexColumn_ da chamada para a função [CreateTable,](createtable.md) que acessa a implementação [de ITableData.](itabledataiunknown.md) 
    
 _lppSRow_
  
> [out] Um ponteiro para um ponteiro para a linha recuperada. 
    
 _lpuliRow_
  
> [in, out] Na entrada, um ponteiro válido ou NULL, que indica que nenhuma informação precisa ser retornada. Na saída, um ponteiro válido que aponta para o número da linha, um número sequencial que identifica a posição da linha na tabela.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A linha foi recuperada com êxito.
    
MAPI_E_INVALID_PARAMETER 
  
> A [estrutura SPropValue](spropvalue.md) para a  _qual lpSPropValue_ aponta não contém a propriedade da coluna de índice. 
    
## <a name="remarks"></a>Comentários

O método **ITableData::HrQueryRow** recupera todas as propriedades da linha que tem uma coluna de índice que corresponde ao valor da coluna de índice incluída na estrutura de propriedades apontada por  _lpSPropValue_. **HrQueryRow** também retorna o número da linha, se o chamador solicitar, que identifica a posição da linha na tabela. 
  
Como **HrQueryRow** não modifica a estrutura **SPropValue** apontada por  _lpSPropValue_, os chamadores devem liberar a estrutura **quando HrQueryRow** retornar. Os chamadores também devem liberar a **estrutura SRow** que contém a linha recuperada. 
  
## <a name="see-also"></a>Confira também



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropValue](spropvalue.md)
  
[SRow](srow.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

