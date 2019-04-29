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
ms.openlocfilehash: 4f5d6a5d2dbb48a86363896bf14b61ed28118330
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422660"
---
# <a name="mapi-interfaces"></a>Interfaces MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A documentação de cada interface consiste em uma seção introdutória que inclui uma breve descrição da finalidade da interface, seguida de uma tabela que contém as informações a seguir.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |O arquivo de cabeçalho onde a interface é definida e que deve ser incluída quando você compila o código-fonte.  <br/> |
|Exposto por:  <br/> |O objeto que expõe a interface.  <br/> |
|Implementado por:  <br/> |Uma lista dos componentes que fornecem uma implementação da interface.  <br/> |
|Chamado por:  <br/> |Uma lista dos componentes que normalmente chamam os métodos da interface.  <br/> |
|Identificador de interface:  <br/> |O GUID do identificador de interface.  <br/> |
|Tipo de ponteiro:  <br/> |O tipo de ponteiro para o objeto que expõe a interface.  <br/> |
|Modelo de transação:  <br/> |Para interfaces derivadas de [IMAPIProp](imapipropiunknown.md). Se não realizadas, as alterações terão efeito imediatamente; se transacionado, as alterações não entrarão em vigor até que [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) seja chamado.  <br/> |
   
A seguir, a primeira tabela é outra tabela que lista todos os métodos dessa interface em ordem vtable. Uma vtable é uma matriz de ponteiros de função criado pelo compilador que contém um ponteiro de função para cada método de um objeto MAPI. Os métodos estão listados na mesma ordem em que são declarados. Os métodos herdados de outras interfaces não são mostrados na tabela de pedidos vtable, mas podem ser usados da mesma maneira como documentados na interface que os define.
  
Após cada tópico de interface, os métodos da interface são documentados em ordem alfabética. Para cada método, a documentação inclui uma instrução de curto objetivo, um bloco de sintaxe e as informações a seguir.
  
|**Título**|**Conteúdo**|
|:-----|:-----|
|Parâmetros  <br/> |Uma descrição de cada parâmetro no método.  <br/> |
|Valor de retorno  <br/> |Uma descrição dos valores exclusivos que o método pode retornar. Estes são os valores que os chamadores devem verificar no código.  <br/> |
|Comentários  <br/> |Uma descrição do porquê e como o método é usado.  <br/> |
|Confira também  <br/> |Referências cruzadas para outros tópicos nesta referência.  <br/> |
   
## <a name="see-also"></a>Confira também



[Referencia MAPI](mapi-reference.md)

