---
title: IMAPITableFindRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.FindRow
api_type:
- COM
ms.assetid: 6511368c-9777-497e-9eea-cf390c04b92e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a5364af229721d101f38d2f054f528169b48c09e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429569"
---
# <a name="imapitablefindrow"></a>IMAPITable::ExpandRow

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Localiza a próxima linha em uma tabela que corresponde a critérios de pesquisa específicos e move o cursor para essa linha.
  
```cpp
HRESULT FindRow(
LPSRestriction lpRestriction,
BOOKMARK BkOrigin,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpRestriction_
  
> [in] Um ponteiro para uma [estrutura SRestriction](srestriction.md) que descreve os critérios de pesquisa. 
    
 _BkOrigin_
  
> [in] Um indicador que identifica a linha onde **FindRow** deve iniciar sua pesquisa. Um indicador pode ser criado usando o método [IMAPITable::CreateBookmark](imapitable-createbookmark.md) ou um dos seguintes valores predefinidos pode ser passado. 
    
BOOKMARK_BEGINNING 
  
> Pesquisa desde o início da tabela. 
    
BOOKMARK_CURRENT 
  
> Pesquisa a partir da linha na tabela onde o cursor está localizado. 
    
BOOKMARK_END 
  
> Pesquisa a partir do final da tabela. 
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla a direção da pesquisa. O sinalizador a seguir pode ser definido:
    
DIR_BACKWARD 
  
> Pesquisa para trás a partir da linha identificada pelo indicador.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A operação de encontrar foi bem-sucedida.
    
MAPI_E_INVALID_BOOKMARK 
  
> O indicador no parâmetro  _BkOrigin_ é inválido porque foi removido ou porque está além da última linha solicitada. 
    
MAPI_E_NOT_FOUND 
  
> Não foram encontradas linhas que corresponderam à restrição.
    
MAPI_W_POSITION_CHANGED
  
> A chamada foi bem-sucedida, mas o indicador usado na operação não está mais definido na mesma linha de quando foi usada pela última vez; se o indicador não tiver sido usado, ele não está mais na mesma posição de quando foi criado. Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse aviso, use a **HR_FAILED** macro. Consulte [Usando macros para tratamento de erros.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Comentários

O método **IMAPITable::FindRow** localiza a primeira linha na tabela para corresponder a um conjunto de critérios de pesquisa descritos na estrutura **SRestriction** apontada pelo parâmetro _lpRestriction._ 
  
Normalmente, **FindRow** pesquisa para frente a partir do indicador especificado. O chamador pode definir a pesquisa para mover para trás do indicador definindo o sinalizador DIR_BACKWARD no _parâmetro ulFlags._ A pesquisa para frente começa a partir do indicador atual; a pesquisa para trás começa a partir da linha anterior ao indicador. A posição final da pesquisa é logo antes da primeira linha encontrada que satisfez a restrição. 
  
Se a linha apontada pelo indicador no parâmetro  _BkOrigin_ não existir mais na tabela e a tabela não puder estabelecer uma nova posição para o indicador, **FindRow** retornará MAPI_E_INVALID_BOOKMARK. Se a linha apontada por  _BkOrigin_ não existir mais e a tabela for capaz de estabelecer uma nova posição para o indicador, **FindRow** retornará MAPI_W_POSITION_CHANGED. 
  
Se o indicador passado em  _BkOrigin_ for BOOKMARK_BEGINNING ou BOOKMARK_END, **FindRow** retornará MAPI_E_NOT_FOUND se nenhuma linha correspondente for encontrada. Se o indicador usado em  _BkOrigin_ for BOOKMARK_CURRENT, **FindRow** poderá retornar MAPI_W_POSITION_CHANGED mas não MAPI_E_INVALID_BOOKMARK porque sempre haverá uma posição atual do cursor. 
  
A **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) é necessária para todas as tabelas, e todas as implementações de **FindRow** são necessárias para dar suporte a chamadas que buscam uma linha com base em PR_INSTANCE_KEY. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

O tipo de pesquisa de prefixo realizada pela **FindRow** só é útil quando a pesquisa segue a mesma direção que a organização da tabela. Para obter o comportamento necessário, a função de comparação implícita pelo **RELOP_GE** passado na estrutura de restrição de propriedade deve ser a mesma função de comparação na qual a ordem de classificação da tabela se baseia. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode usar **FindRow para** dar suporte à rolagem com base em cadeias de caracteres digitadas pelo usuário, especialmente em caixas de listagem nas caixas de diálogo de endereço. Nesse tipo de rolagem, os usuários ins digitam prefixos progressivamente mais longos de um valor de cadeia de caracteres desejado e você pode emitir periodicamente uma chamada **FindRow** para ir para a primeira linha que corresponde ao prefixo. A direção para a qual o cursor vai depende de qual direção a pesquisa está definida para executar. 
  
Para usar **FindRow,** um indicador deve ser definido. A pesquisa de cadeia de caracteres pode se originar de qualquer indicador, inclusive dos indicadores predefinidos que indicam a posição atual e o início e o fim da tabela. Se houver um grande número de linhas na tabela, a operação de pesquisa poderá ser lenta.
  
Use uma restrição para encontrar um prefixo de cadeia de caracteres para rolagem da seguinte forma. Para pesquisa direta em uma coluna ordenada em ordem crescente e para pesquisa regressiva em uma coluna ordenada em ordem decrescente, passe uma estrutura de restrição  de propriedade no parâmetro _lpRestriction_ com a relação RELOP_GE e o prefixo e **marca** de propriedade apropriada, usando o _prefixo_ de marca de formato **GE** . 
  
Para obter mais informações sobre como usar estruturas de restrição para especificar um filtro, consulte [Sobre restrições.](about-restrictions.md)
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI usa o **método IMAPITable::FindRow** para encontrar linhas que corresponderem a uma restrição.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[SRestriction](srestriction.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

