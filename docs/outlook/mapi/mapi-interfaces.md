---
title: Interfaces MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 34a66cf0-b4e0-4fd5-b937-cd157888961d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ca3752e8f7e910994811dec85cc2f1b00e184661
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584804"
---
# <a name="mapi-interfaces"></a>Interfaces MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A documentação para cada interface consiste em uma seção introdutória que inclui uma breve descrição do objetivo da interface seguido de uma tabela que contém as seguintes informações.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |O arquivo de cabeçalho onde a interface é definida e que deve ser incluído quando você compila seu código-fonte.  <br/> |
|Expostos pelo:  <br/> |O objeto que expõe a interface.  <br/> |
|Implementado por:  <br/> |Uma lista dos componentes que oferecem uma implementação da interface.  <br/> |
|Chamado por:  <br/> |Uma lista dos componentes que geralmente chame os métodos da interface.  <br/> |
|Identificador de interface:  <br/> |O identificador de interface GUID.  <br/> |
|Tipo de ponteiro:  <br/> |O tipo de ponteiro para o objeto que expõe a interface.  <br/> |
|Modelo de transação:  <br/> |Para interfaces derivado do [IMAPIProp](imapipropiunknown.md). Se nontransacted, as alterações entrem em vigor imediatamente; Se transacionadas, as alterações não entrarão em vigor até que [IMAPIProp::SaveChanges](imapiprop-savechanges.md) seja chamado.  <br/> |
   
A primeira tabela a seguir é outra tabela que lista todos os métodos dessa interface na ordem vtable. Uma vtable é uma matriz de indicadores de função criado pelo compilador que contém um ponteiro de função para cada método de um objeto MAPI. Os métodos são listados na mesma ordem em que eles são declarados. Métodos herdados de outras interfaces não são mostrados na tabela a ordem Vtable, mas podem ser usados da mesma forma, conforme documentado na interface do que as define.
  
Após cada tópico interface, os métodos da interface estão documentados, em seguida, em ordem alfabética. Para cada método, a documentação inclui uma instrução de finalidade breve, um bloco de sintaxe e as informações a seguir.
  
|**Título**|**Conteúdo**|
|:-----|:-----|
|Parâmetros  <br/> |Uma descrição de cada parâmetro do método.  <br/> |
|Valor retornado  <br/> |Uma descrição dos valores exclusivos que o método pode ser retornado. Estes são os valores que os chamadores devem verificar se há em seu código.  <br/> |
|Comentários  <br/> |Uma descrição do porque e como o método é usado.  <br/> |
|Consulte também  <br/> |Referências cruzadas para outros tópicos nesta referência.  <br/> |
   
## <a name="see-also"></a>Confira também



[Refer�ncia MAPI (em ingl�s)](mapi-reference.md)

