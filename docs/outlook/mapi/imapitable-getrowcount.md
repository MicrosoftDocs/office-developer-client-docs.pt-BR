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
ms.openlocfilehash: b13bf3bdd8392efc42ad189e48dffad8636f0708
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425600"
---
# <a name="imapitablegetrowcount"></a>IMAPITable::GetRowCount

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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
  
> [out] Ponteiro para o número de linhas na tabela.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A contagem de linhas foi retornada com êxito.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento que impede o início da operação de recuperação de contagem de linhas. A operação em andamento deve ter permissão para ser concluída ou deve ser interrompida.
    
MAPI_E_NO_SUPPORT 
  
> A tabela não pode calcular o número de linhas.
    
MAPI_W_APPROX_COUNT 
  
> A chamada foi bem-sucedida, mas uma contagem aproximada de linhas foi retornada porque a contagem exata de linhas não pôde ser determinada possivelmente devido a restrições de memória. Para testar esse aviso, use a **HR_FAILED** macro. Consulte [Usando macros para tratamento de erros.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Comentários

O **método IMAPITable::GetRowCount** recupera o número total de linhas em uma tabela. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Se não for possível determinar a contagem exata de linhas da tabela, retorne MAPI_W_APPROX_COUNT uma contagem aproximada de linhas no conteúdo do parâmetro _lpulCount._ 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Use **GetRowCount** para descobrir quantas linhas uma tabela contém antes de fazer uma chamada para o método [IMAPITable::QueryRows](imapitable-queryrows.md) para recuperar os dados. Se houver menos de vinte linhas na tabela, é seguro chamar **QueryPosition** para recuperar a tabela inteira. Se houver mais de vinte linhas na tabela, considere fazer várias chamadas para **QueryPosition** e limite o número de linhas recuperadas em cada chamada. 
  
Algumas tabelas não suportam **GetRowCount** e retornam MAPI_E_NO_SUPPORT. Se **GetRowCount** não tiver suporte, uma alternativa pode ser chamar [IMAPITable::QueryPosition](imapitable-queryposition.md). Com os resultados de **QueryPosition**, você pode determinar a relação entre a linha atual e a última linha. 
  
Quando **GetRowCount** retornar MAPI_E_BUSY porque não é possível recuperar temporariamente uma contagem de linhas, chame o método [IMAPITable::WaitForCompletion.](imapitable-waitforcompletion.md) Quando **WaitForCompletion** retornar, repetir a chamada para **GetRowCount**. Outra maneira de detectar se uma operação assíncrona está em andamento é chamar o método [IMAPITable::GetStatus](imapitable-getstatus.md) e verificar o conteúdo do parâmetro _lpulTableState._ 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CopyFolderContents  <br/> |MFCMAPI usa o método **IMAPITable::GetRowCount** para determinar quantas linhas estão na tabela de origem para que a memória possa ser alocada para executar a cópia.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::QueryPosition](imapitable-queryposition.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

