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
|Arquivo de cabeçalho:  <br/> |O arquivo de header em que a interface está definida e que deve ser incluído ao compilar o código-fonte.  <br/> |
|Exposto por:  <br/> |O objeto que expõe a interface.  <br/> |
|Implementado por:  <br/> |Uma lista dos componentes que fornecem uma implementação da interface.  <br/> |
|Chamado por:  <br/> |Uma lista dos componentes que normalmente chamam os métodos da interface.  <br/> |
|Identificador de interface:  <br/> |O GUID do identificador da interface.  <br/> |
|Tipo de ponteiro:  <br/> |O tipo de ponteiro para o objeto que expõe a interface.  <br/> |
|Modelo de transação:  <br/> |Para interfaces derivadas de [IMAPIProp](imapipropiunknown.md). Se não for traduzida, as alterações vigorarão imediatamente; se transacionado, as alterações não são efetivadas até [que IMAPIProp::SaveChanges](imapiprop-savechanges.md) seja chamado.  <br/> |
   
Após a primeira tabela, há outra tabela que lista todos os métodos dessa interface em ordem vtable. Uma vtable é uma matriz de ponteiros de função criada pelo compilador contendo um ponteiro de função para cada método de um objeto MAPI. Os métodos são listados na mesma ordem em que são declarados. Os métodos herdados de outras interfaces não são mostrados na tabela Ordem da Tabela Vtable, mas podem ser usados da mesma maneira que documentados na interface que os define.
  
Após cada tópico da interface, os métodos da interface são documentados em ordem alfabética. Para cada método, a documentação inclui uma breve instrução de finalidade, um bloco de sintaxe e as informações a seguir.
  
|**Título**|**Conteúdo**|
|:-----|:-----|
|Parâmetros  <br/> |Uma descrição de cada parâmetro no método.  <br/> |
|Valor de retorno  <br/> |Uma descrição dos valores exclusivos que o método pode retornar. Esses são os valores que os chamadores devem verificar em seu código.  <br/> |
|Comentários  <br/> |Uma descrição do motivo e de como o método é usado.  <br/> |
|Confira também  <br/> |Referências cruzadas a outros tópicos nesta referência.  <br/> |
   
## <a name="see-also"></a>Confira também



[Referencia MAPI](mapi-reference.md)

