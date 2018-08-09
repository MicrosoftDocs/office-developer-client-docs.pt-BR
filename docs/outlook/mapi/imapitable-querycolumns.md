---
title: IMAPITableQueryColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryColumns
api_type:
- COM
ms.assetid: d6341acc-c6ca-4605-93af-77230040339d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 96fd317c28d95335a3acc5d0603298f2fe8345e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767336"
---
# <a name="imapitablequerycolumns"></a>IMAPITable::QueryColumns

  
  
**Aplica-se a**: Outlook 
  
Retorna uma lista das colunas da tabela.
  
```cpp
HRESULT QueryColumns(
ULONG ulFlags,
LPSPropTagArray FAR * lpPropTagArray
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Bitmask dos sinalizadores que indica qual coluna conjunto deve ser retornada. O seguinte sinalizador pode ser definido:
    
TBL_ALL_COLUMNS 
  
> A tabela deve retornar todas as colunas disponíveis.
    
 _lpPropTagArray_
  
> [out] Ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém as marcas de propriedade para a coluna definido. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O conjunto de coluna foi retornado com êxito.
    
MAPI_E_BUSY 
  
> Outra operação é em andamento que impeça a coluna definida a operação de recuperação seja iniciado. Ou a operação em andamento deve ter permissão para concluir ou ele deve ser interrompido.
    
## <a name="remarks"></a>Comentários

O método **IMAPITable::QueryColumns** pode ser chamado para recuperar: 
  
- Coluna padrão definido para uma tabela.
    
- A coluna atual definido para uma tabela, conforme estabelecido por uma chamada ao método [IMAPITable::SetColumns](imapitable-setcolumns.md) . 
    
- A coluna completa definidas para uma tabela, as colunas que estão disponíveis, mas não necessariamente parte do conjunto atual.
    
## <a name="notes-to-callers"></a>Notas para chamadores

Se você não definir o sinalizador TBL_ALL_COLUMNS, **IMAPITable::QueryColumns** retorna padrão uma tabela ou conjunto de coluna atual, dependendo se a tabela foi afetada por uma chamada para **IMAPITable::SetColumns**. **SetColumns** altera o sentido e seleção de colunas no conjunto de colunas de uma tabela. 
  
Se você definir o sinalizador TBL_ALL_COLUMNS, **QueryColumns** retorna todas as colunas que são capazes de sendo no conjunto de coluna da tabela. 
  
Libere a memória para a matriz de marca de propriedade apontada pelo parâmetro _lpPropTagArray_ chamando a função [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::DoSetColumns  <br/> |MFCMAPI usa o método **IMAPITable::QueryColumns** para recuperar a coluna atual, definido para uma tabela para que o usuário possa ser editado.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

