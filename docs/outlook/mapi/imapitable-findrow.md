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
  
> no Um ponteiro para uma estrutura [SRestriction](srestriction.md) que descreve os critérios de pesquisa. 
    
 _BkOrigin_
  
> no Um indicador identificando a linha onde o **FindRow** deve começar sua pesquisa. Um indicador pode ser criado usando o método imApitable [:: CreateBookmark](imapitable-createbookmark.md) ou um dos seguintes valores predefinidos pode ser passado. 
    
BOOKMARK_BEGINNING 
  
> Pesquisa a partir do início da tabela. 
    
BOOKMARK_CURRENT 
  
> Pesquisa a partir da linha na tabela onde o cursor está localizado. 
    
BOOKMARK_END 
  
> Pesquisa a partir do final da tabela. 
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controlam a direção da pesquisa. O seguinte sinalizador pode ser definido:
    
DIR_BACKWARD 
  
> Pesquisa retroativa a partir da linha identificada pelo indicador.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A operação de localização foi bem-sucedida.
    
MAPI_E_INVALID_BOOKMARK 
  
> O indicador no parâmetro _BkOrigin_ é inválido porque foi removido ou porque está além da última linha solicitada. 
    
MAPI_E_NOT_FOUND 
  
> Nenhuma linha que correspondeu à restrição foi encontrada.
    
MAPI_W_POSITION_CHANGED
  
> A chamada foi bem-sucedida, mas o indicador usado na operação não é mais definido na mesma linha que o quando foi usado pela última vez; Se o indicador não tiver sido usado, ele não estará mais na mesma posição de quando foi criado. Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse aviso, use a macro **HR_FAILED** . Consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentários

O método imApitable **:: FindRow** localiza a primeira linha na tabela para corresponder a um conjunto de critérios de pesquisa descritos na estrutura **SRestriction** apontada pelo parâmetro _lpRestriction_ . 
  
Normalmente, as pesquisas de **FindRow** são revertidas a partir do indicador especificado. O chamador pode definir a pesquisa para mover para trás do indicador definindo o sinalizador DIR_BACKWARD no parâmetro _parâmetroulflags_ . A pesquisa antecipada começa no indicador atual; a pesquisa de versões anteriores começa da linha anterior ao indicador. A posição final da pesquisa é anterior à primeira linha encontrada e satisfeita na restrição. 
  
Se a linha indicada pelo indicador no parâmetro _BkOrigin_ não existir mais na tabela e a tabela não puder estabelecer uma nova posição para o indicador, **FindRow** retornará MAPI_E_INVALID_BOOKMARK. Se a linha indicada por _BkOrigin_ não existir mais e a tabela puder estabelecer uma nova posição para o indicador, **FindRow** retornará MAPI_W_POSITION_CHANGED. 
  
Se o indicador passado no _BkOrigin_ for BOOKMARK_BEGINNING ou BOOKMARK_END, **FindRow** retornará MAPI_E_NOT_FOUND se nenhuma linha correspondente for encontrada. Se o indicador usado no _BkOrigin_ for BOOKMARK_CURRENT, **FINDROW** poderá retornar MAPI_W_POSITION_CHANGED, mas não MAPI_E_INVALID_BOOKMARK, porque sempre há uma posição de cursor atual. 
  
A coluna da propriedade **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) é necessária para todas as tabelas, e todas as implementações de **FindRow** são necessárias para dar suporte a chamadas que buscam uma linha com base no PR_INSTANCE_KEY. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

O tipo de pesquisa de prefixo realizado pelo **FindRow** só é útil quando a pesquisa segue a mesma direção da organização da tabela. Para obter o comportamento necessário, a função de comparação inferida pelo **RELOP_GE** passado na estrutura de restrição de propriedade deve ser a mesma função de comparação na qual a ordem de classificação da tabela se baseia. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode usar o **FindRow** para dar suporte à rolagem com base em cadeias de caracteres digitadas pelo usuário, especialmente nas caixas de listagem nas caixas de diálogo de endereço. Nesse tipo de rolagem, os usuários inserem prefixos cada vez mais longos de um valor de cadeia de caracteres desejado e você pode emitir periodicamente uma chamada **FindRow** para saltar para a primeira linha que corresponde ao prefixo. Qual direção o cursor salta depende da direção em que a pesquisa está definida para executar. 
  
Para usar **FindRow**, um indicador deve ser definido. A pesquisa de cadeia de caracteres pode ser originada de qualquer indicador, incluindo os indicadores predefinidos que indicam a posição atual e o início e o fim da tabela. Se houver um grande número de linhas na tabela, a operação de pesquisa poderá ser lenta.
  
Use uma restrição para localizar um prefixo de cadeia de caracteres para a rolagem da seguinte maneira. Para encaminhar a pesquisa em uma coluna classificada em ordem crescente e para pesquisa retroativa em uma coluna classificada em ordem decrescente, passe uma estrutura de restrição de propriedade no parâmetro _lpRestriction_ com a relação **RELOP_GE** e as marca de propriedade e prefixo, usando o __ **** _prefixo_GE da marca de formatação. 
  
Para obter mais informações sobre como usar estruturas de restrição para especificar um filtro, consulte [about Restrictions](about-restrictions.md).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI usa o método imApitable **:: FindRow** para localizar linhas que correspondem a uma restrição.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[SRestriction](srestriction.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

