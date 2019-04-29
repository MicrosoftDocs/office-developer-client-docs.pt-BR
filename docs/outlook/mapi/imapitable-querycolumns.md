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
ms.openlocfilehash: d142e19fc4721cec4dde0df7fc030a001121da63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410102"
---
# <a name="imapitablequerycolumns"></a>IMAPITable::QueryColumns

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna uma lista de colunas da tabela.
  
```cpp
HRESULT QueryColumns(
ULONG ulFlags,
LPSPropTagArray FAR * lpPropTagArray
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Bitmask de sinalizadores que indica o conjunto de colunas que deve ser retornado. O seguinte sinalizador pode ser definido:
    
TBL_ALL_COLUMNS 
  
> A tabela deve retornar todas as colunas disponíveis.
    
 _lpPropTagArray_
  
> bota Ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém as marcas de propriedade para o conjunto de colunas. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O conjunto de colunas foi retornado com êxito.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento, o que impede a inicialização da operação de recuperação do conjunto de colunas. A operação em andamento deve ter permissão para ser concluída ou deve ser interrompida.
    
## <a name="remarks"></a>Comentários

O método imApitable **:: QueryColumns** pode ser chamado para recuperar: 
  
- A coluna padrão definida para uma tabela.
    
- A coluna atual definida para uma tabela, conforme estabelecida por uma chamada para o método imApitable [::](imapitable-setcolumns.md) SetColumns. 
    
- A coluna completa definida para uma tabela, as colunas que estão disponíveis, mas não necessariamente fazem parte do conjunto atual.
    
## <a name="notes-to-callers"></a>Notas para chamadores

Se você não definir o sinalizador TBL_ALL_COLUMNS, imApitable **:: QueryColumns** retorna o conjunto de colunas padrão ou atual da tabela, dependendo se a tabela foi afetada por uma chamada a IMAPITable **::** SetColumns. **** SetColumns altera a ordem e a seleção de colunas no conjunto de colunas de uma tabela. 
  
Se você definir o sinalizador TBL_ALL_COLUMNS, **QueryColumns** retornará todas as colunas que forem capazes de estar no conjunto de colunas da tabela. 
  
Libere a memória para a matriz de marca de propriedade apontada pelo parâmetro _lpPropTagArray_ chamando a função [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |CContentsTableListCtrl::D oSetColumns  <br/> |MFCMAPI usa o método imApitable **:: QueryColumns** para recuperar o conjunto de colunas atual para uma tabela para que o usuário possa editá-lo.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

