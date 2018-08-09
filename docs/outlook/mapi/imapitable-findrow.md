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
ms.openlocfilehash: cb777074d1657a3ee5c2f1e9f70d2b304858c1b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767324"
---
# <a name="imapitablefindrow"></a>IMAPITable::ExpandRow

  
  
**Aplica-se a**: Outlook 
  
Localiza a próxima linha em uma tabela que corresponde a determinados critérios de pesquisa e move o cursor para essa linha.
  
```cpp
HRESULT FindRow(
LPSRestriction lpRestriction,
BOOKMARK BkOrigin,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpRestriction_
  
> [in] Um ponteiro para uma estrutura de [SRestriction](srestriction.md) que descreve os critérios de pesquisa. 
    
 _BkOrigin_
  
> [in] Um indicador que identifica a linha onde **FindRow** deve começar sua pesquisa. Um indicador pode ser criado usando o método [IMAPITable::CreateBookmark](imapitable-createbookmark.md) ou um dos seguintes valores predefinidos pode ser passado. 
    
BOOKMARK_BEGINNING 
  
> Pesquisas desde o início da tabela. 
    
BOOKMARK_CURRENT 
  
> Pesquisas da linha da tabela onde o cursor está localizado. 
    
BOOKMARK_END 
  
> Pesquisas da extremidade da tabela. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla a direção da pesquisa. O seguinte sinalizador pode ser definido:
    
DIR_BACKWARD 
  
> Pesquisa para trás da linha identificada pelo indicador.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A operação de localização foi bem-sucedida.
    
MAPI_E_INVALID_BOOKMARK 
  
> O indicador no parâmetro _BkOrigin_ é inválido porque ele foi removido ou está além da última linha solicitada. 
    
E_NOT_FOUND 
  
> Nenhuma linha foram encontrada que correspondem a restrição.
    
MAPI_W_POSITION_CHANGED
  
> A chamada foi bem-sucedida, mas o indicador usado na operação não é mais é definido na mesma linha que quando ele foi usado por último; Se o indicador não tiver sido usado, ele não está mais na mesma posição quando ele foi criado. Quando esse aviso é retornado, a chamada deve ser manipulada com êxito. Para testar esse aviso, use a macro **HR_FAILED** . Consulte [usando Macros para tratamento de erros](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentários

O método **IMAPITable:: FindRow** localiza a primeira linha da tabela para coincidir com um conjunto de critérios de pesquisa descrito na estrutura **SRestriction** apontada pelo parâmetro _lpRestriction_ . 
  
Geralmente, **FindRow** pesquisa frente do indicador especificado. O chamador pode definir a pesquisa Retroceder do indicador, definindo o sinalizador DIR_BACKWARD no parâmetro _ulFlags_ . Encaminhar a pesquisa começa a partir do indicador atual; Pesquisar para trás começa a partir da linha antes do indicador. A posição final da pesquisa é pouco antes da primeira linha encontrada que satisfeito a restrição. 
  
Se a linha apontada pelo indicador no parâmetro _BkOrigin_ não existe mais na tabela e a tabela não é possível estabelecer uma nova posição para o indicador, **FindRow** retorna MAPI_E_INVALID_BOOKMARK. Se a linha apontada pela _BkOrigin_ não existe mais e a tabela é capaz de estabelecer uma nova posição para o indicador, **FindRow** retorna MAPI_W_POSITION_CHANGED. 
  
Se o indicador passado em _BkOrigin_ for BOOKMARK_BEGINNING ou BOOKMARK_END, **FindRow** retorna E_NOT_FOUND se sem linha correspondente for encontrada. Se o indicador usado em _BkOrigin_ for BOOKMARK_CURRENT, **FindRow** pode retornar MAPI_W_POSITION_CHANGED, mas não MAPI_E_INVALID_BOOKMARK porque não há sempre uma posição atual do cursor. 
  
A coluna de propriedade **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) é necessária para todas as tabelas e todas as implementações de **FindRow** são necessárias para dar suporte a chamadas que buscam uma linha com base em PR_INSTANCE_KEY. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

O tipo de prefixo pesquisando executadas pelos **FindRow** só é útil quando a pesquisa segue a mesma direção da organização da tabela. Para atingir o comportamento necessário, a função de comparação implicada **RELOP_GE** passado na estrutura de restrição de propriedade deve ser a mesma função de comparação em que baseia-se a ordem de classificação de tabela. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode usar **FindRow** para suporte a rolagem com base em cadeias de caracteres digitadas pelo usuário, especialmente nas caixas de listagem em caixas de diálogo de endereço. Nesse tipo de rolagem, os usuários insiram prefixos progressivamente mais de um valor de cadeia de caracteres desejado e você pode emitir periodicamente uma chamada **FindRow** saltar à primeira linha que corresponde ao prefixo. Direção saltos do cursor depende de qual direção a pesquisa é definido para ser executado. 
  
Para usar **FindRow**, um indicador deve ser definido. A pesquisa de cadeia de caracteres pode ser originado de qualquer indicador, inclusive os indicadores predefinidos, que indica a posição atual e o início e fim da tabela. Se houver um grande número de linhas da tabela, a operação de pesquisa pode ser lenta.
  
Use uma restrição para encontrar um prefixo de cadeia de caracteres para a rolagem da seguinte maneira. Para encaminhar a pesquisa em uma coluna classificada em ordem crescente e para a pesquisa para trás em uma coluna classificada em ordem decrescente, passe uma estrutura de restrição de propriedade no parâmetro _lpRestriction_ com relação a **RELOP_GE** e apropriada marca de propriedade e prefixo, usando o formato _tag_ **GE** _prefixo_. 
  
Para obter mais informações sobre como usar as estruturas de restrição para especificar um filtro, consulte [Sobre restrições](about-restrictions.md).
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI usa o método **IMAPITable:: FindRow** para localizar linhas que correspondam a uma restrição.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[SRestriction](srestriction.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

