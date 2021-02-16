---
title: IMAPITableSeekRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SeekRow
api_type:
- COM
ms.assetid: 93ac63ae-f254-45e1-a9b1-347d69d2ed9f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fbc990a8c962883aa07987b200d1d2fd55434f93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413042"
---
# <a name="imapitableseekrow"></a>IMAPITable::SeekRow

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Move o cursor para uma posição específica na tabela.
  
```cpp
HRESULT SeekRow(
BOOKMARK bkOrigin,
LONG lRowCount,
LONG FAR * lplRowsSought
);
```

## <a name="parameters"></a>Parâmetros

 _bkOrigin_
  
> [in] O indicador que identifica a posição inicial da operação de busca. Um indicador pode ser criado usando o método [IMAPITable::CreateBookmark](imapitable-createbookmark.md) ou um dos seguintes valores predefinidos pode ser passado. 
    
BOOKMARK_BEGINNING 
  
> Inicia a operação de busca desde o início da tabela. 
    
BOOKMARK_CURRENT 
  
> Inicia a operação de busca a partir da linha na tabela onde o cursor está localizado. 
    
BOOKMARK_END 
  
> Inicia a operação de busca no final da tabela. 
    
 _lRowCount_
  
> [in] A contagem assinada do número de linhas a mover, começando pelo indicador identificado pelo _parâmetro bkOrigin._ 
    
 _lplRowsSought_
  
> [out] Se  _lRowCount_ for um ponteiro válido na entrada,  _lplRowsSought_ apontará para o número de linhas que foram processadas na operação de busca, o sinal indicando a direção da pesquisa, para frente ou para trás. Se  _lRowCount_ for negativo,  _lplRowsSought_ será negativo. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A operação de busca foi bem-sucedida.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento que impede o início da operação de busca de linhas. A operação em andamento deve ter permissão para ser concluída ou deve ser interrompida.
    
MAPI_E_INVALID_BOOKMARK 
  
> O indicador especificado no parâmetro  _bkOrigin_ é inválido porque foi removido ou porque está além da última linha solicitada. 
    
MAPI_W_POSITION_CHANGED 
  
> A chamada foi bem-sucedida, mas o indicador especificado no parâmetro  _bkOrigin_ não é mais definido na mesma linha que estava quando foi usada pela última vez. Se o indicador não tiver sido usado, ele não está mais na mesma posição que estava quando foi criado. Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse aviso, use a **HR_FAILED** macro. Para obter mais informações, consulte [Usando macros para tratamento de erros.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Comentários

O **método IMAPITable::SeekRow** estabelece uma nova BOOKMARK_CURRENT para o cursor. O  _parâmetro lRowCount_ indica o número de linhas que o cursor move e a direção do movimento. 
  
Se a posição resultante estiver além da última linha da tabela, o cursor será posicionado após a última linha. Se a posição resultante estiver antes da primeira linha da tabela, o cursor será posicionado no início da primeira linha. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Se a linha apontada por  _bkOrigin_ não existir mais na tabela e você não puder estabelecer uma nova posição para o indicador, retorne MAPI_E_INVALID_BOOKMARK. Se a linha apontada por  _bkOrigin_ não existir mais e você puder estabelecer uma nova posição para o indicador, retorne MAPI_W_POSITION_CHANGED. 
  
Um indicador apontando para uma linha que está recolhido para fora do ponto de vista da tabela ainda pode ser usado. Se o chamador tentar mover o cursor para esse indicador, mova o cursor para a próxima linha visível e retorne MAPI_W_POSITION_CHANGED. 
  
Você pode mover indicadores para posições recolhidos para fora da exibição, seja no momento do uso ou no momento em que a linha é colada. Se um indicador for movido no momento em que a linha estiver recolhido, mantenha um pouco no indicador que indica se o indicador foi movido desde seu último uso ou, se nunca foi usado, desde sua criação.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para indicar um movimento para trás **para SeekRow**, passe um valor negativo em  _lRowCount_. Para pesquisar no início da tabela, passe zero em  _lRowCount_ e o valor BOOKMARK_BEGINNING  _em bkOrigin_. 
  
Se houver muitas linhas na tabela, a operação **SeekRow** poderá ser lenta. O desempenho também pode ser afetado se você precisar que uma contagem de linhas seja retornada no conteúdo do _parâmetro lplRowsSought._ 
  
 **SeekRow** retorna o número de linhas pesquisadas, positivas ou negativas, na variável apontada por  _lRowCount_. Em uma operação comum, ele deve retornar o mesmo valor de  _lplRowsSought_ como passado para  _lRowCount_, a menos que a pesquisa tenha atingido o início ou o fim da tabela. 
  
Não de definir  _lRowCount como_ um número maior que 50. Para procurar um número maior de linhas, use o [método IMAPITable::SeekRowApprox.](imapitable-seekrowapprox.md) 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIProcessor.cpp  <br/> |CMAPIProcessor::P rocessMailboxTable  <br/> |MFCMAPI usa o **método IMAPITable::SeekRow** para localizar o início da tabela antes do processamento.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::ExpandRow](imapitable-findrow.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

