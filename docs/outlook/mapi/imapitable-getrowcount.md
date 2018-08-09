---
title: IMAPITableGetRowCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetRowCount
api_type:
- COM
ms.assetid: 44a12c92-7462-4acf-9520-5d4c2d7f1d47
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a591a49c1cb0ec936d09d59b4632d15e4842dd2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767337"
---
# <a name="imapitablegetrowcount"></a>IMAPITable::GetRowCount

  
  
**Aplica-se a**: Outlook 
  
Retorna o número total de linhas na tabela. 
  
```cpp
HRESULT GetRowCount(
ULONG ulFlags,
ULONG FAR * lpulCount
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> Reservado; deve ser zero.
    
 _lpulCount_
  
> [out] Ponteiro para o número de linhas da tabela.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A contagem de linhas foi retornada com êxito.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento que impede que a operação de recuperação de contagem de linha seja iniciado. Ou a operação em andamento deve ter permissão para concluir ou ele deve ser interrompido.
    
MAPI_E_NO_SUPPORT 
  
> A tabela não é possível calcular o número de linhas.
    
MAPI_W_APPROX_COUNT 
  
> A chamada foi bem-sucedida, mas uma contagem de linhas aproximada foi retornada porque o número exato de linhas não pôde ser determinado possivelmente devido a restrições de memória. Para testar esse aviso, use a macro **HR_FAILED** . Consulte [usando Macros para tratamento de erros](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentários

O método **IMAPITable::GetRowCount** recupera o número total de linhas em uma tabela. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Se você não puder determinar a contagem de exato de linhas da tabela, retorno MAPI_W_APPROX_COUNT e uma linha aproximada contagem no conteúdo do parâmetro _lpulCount_ . 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Usar **GetRowCount** para descobrir quantas linhas uma tabela contém antes de fazer uma chamada para o método [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar os dados. Se houver menos de vinte linhas na tabela, é seguro chamar **QueryPosition** para recuperar a tabela inteira. Se houver mais de vinte linhas da tabela, considere a possibilidade de várias chamadas para **QueryPosition** e limitar o número de linhas recuperadas em cada chamada. 
  
Algumas tabelas não suportam **GetRowCount** e retornar MAPI_E_NO_SUPPORT. Se não há suporte para **GetRowCount** , pode ser uma alternativa chamada [IMAPITable::QueryPosition](imapitable-queryposition.md). Com os resultados do **QueryPosition**, você pode determinar a relação entre a linha atual e a última linha. 
  
Quando **GetRowCount** retorna MAPI_E_BUSY porque ele é temporariamente não é possível recuperar uma contagem de linha, chame o método de [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) . Quando **WaitForCompletion** retorna, repita a chamada para **GetRowCount**. Outra maneira para detectar se uma operação assíncrona está em andamento é chamar o método [IMAPITable::GetStatus](imapitable-getstatus.md) e verifique o conteúdo do parâmetro _lpulTableState_ . 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CopyFolderContents  <br/> |MFCMAPI usa o método **IMAPITable::GetRowCount** para determinar quantas linhas estão na tabela de origem, portanto, é possível alocar memória para realizar a cópia.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::QueryPosition](imapitable-queryposition.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

