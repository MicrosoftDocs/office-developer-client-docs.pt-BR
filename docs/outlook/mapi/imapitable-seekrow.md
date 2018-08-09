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
ms.openlocfilehash: 143ca03a5e98d638d29394f5c0803e349ab4de25
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767340"
---
# <a name="imapitableseekrow"></a>IMAPITable::SeekRow

  
  
**Aplica-se a**: Outlook 
  
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
  
> [in] O indicador que identifica a posição inicial para a operação de busca. Um indicador pode ser criado usando o método [IMAPITable::CreateBookmark](imapitable-createbookmark.md) ou um dos seguintes valores predefinidos pode ser passado. 
    
BOOKMARK_BEGINNING 
  
> Inicia a operação de seek desde o início da tabela. 
    
BOOKMARK_CURRENT 
  
> Inicia a operação de busca da linha da tabela onde o cursor está localizado. 
    
BOOKMARK_END 
  
> Inicia a operação de seek a partir do final da tabela. 
    
 _lRowCount_
  
> [in] A contagem de assinado do número de linhas para mover, iniciando a partir do indicador identificado pelo parâmetro _bkOrigin_ . 
    
 _lplRowsSought_
  
> [out] Se _lRowCount_ for um ponteiro nos pontos de entrada, _lplRowsSought_ para o número de linhas que foram processados na operação seek válido, no sinal de que indica a direção da pesquisa, para frente ou para trás. Se _lRowCount_ for negativo, _lplRowsSought_ for negativo. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A operação de busca foi bem-sucedida.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento que impede que a operação que buscam linha seja iniciado. Ou a operação em andamento deve ter permissão para concluir ou ele deve ser interrompido.
    
MAPI_E_INVALID_BOOKMARK 
  
> O indicador especificado no parâmetro _bkOrigin_ é inválido porque foi removido ou porque está além da última linha solicitada. 
    
MAPI_W_POSITION_CHANGED 
  
> A chamada foi bem-sucedida, mas o indicador especificado no parâmetro _bkOrigin_ não mais é definido na mesma linha como ele era quando ele foi usado por último. Se o indicador não tiver sido usado, ele não está mais na mesma posição como era quando ele foi criado. Quando esse aviso é retornado, a chamada deve ser manipulada com êxito. Para testar esse aviso, use a macro **HR_FAILED** . Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentários

O método **IMAPITable::SeekRow** estabelece uma nova posição BOOKMARK_CURRENT para o cursor. O parâmetro _lRowCount_ indica o número de linhas que move o cursor e a direção da movimentação. 
  
Se a posição resultante for além da última linha da tabela, o cursor é posicionado depois da última linha. Se a posição resultante for antes da primeira linha da tabela, o cursor é posicionado no início da primeira linha. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Se a linha apontada pela _bkOrigin_ não existe mais na tabela, e não será possível estabelecer uma nova posição para o indicador, retorne MAPI_E_INVALID_BOOKMARK. Se a linha apontada pela _bkOrigin_ não existe mais e é possível estabelecer uma nova posição para o indicador, retorne MAPI_W_POSITION_CHANGED. 
  
Um indicador apontando para uma linha que estiver recolhida sem o modo de exibição de tabela ainda pode ser usado. Se o chamador tenta mover o cursor para tal um indicador, mova o cursor para a próxima linha visível e retornar MAPI_W_POSITION_CHANGED. 
  
Você pode mover indicadores posições recolhidas fora do modo de exibição, no momento do uso ou no momento em que a linha é recolhida. Se um indicador for movido no momento em que a linha estiver recolhida, lembre um pouco indicador que indica se o indicador tiver movido desde o último usá-las ou, se ele nunca tiver sido usado, desde sua criação.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para indicar uma movimentação com versões anteriores para **SeekRow**, passe um valor negativo em _lRowCount_. Para pesquisar até o início da tabela, passe zero em _lRowCount_ e o valor BOOKMARK_BEGINNING em _bkOrigin_. 
  
Se houver muitas linhas da tabela, a operação **SeekRow** pode ser lenta. Desempenho também pode ser afetado se você precisar de uma contagem de linhas a serem retornados no conteúdo do parâmetro _lplRowsSought_ . 
  
 **SeekRow** retorna o número de linhas realmente pesquisadas por meio, positivo ou negativo, na variável apontada pela _lRowCount_. Em uma operação comum, ele deve retornar o mesmo valor para _lplRowsSought_ conforme passados para a _lRowCount_, a menos que a pesquisa atingido o início ou fim da tabela. 
  
Não defina _lRowCount_ para um número maior que 50. Para buscar por meio de um número maior de linhas, use o método [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md) . 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIProcessor.cpp  <br/> |CMAPIProcessor::ProcessMailboxTable  <br/> |MFCMAPI usa o método **IMAPITable::SeekRow** para localizar o início da tabela antes do processamento.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::ExpandRow](imapitable-findrow.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

