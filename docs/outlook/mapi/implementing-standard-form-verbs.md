---
title: Implementando verbos de formulário padrão
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6360b86dc23a5404b818f76cb1c2cd10747ef3cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426118"
---
# <a name="implementing-standard-form-verbs"></a>Implementando verbos de formulário padrão

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
MAPI define um conjunto de verbos padrão, ou ações tomadas quando um usuário faz uma seleção de menu ou clica em um botão, que todos os visualizadores de formulário devem suportar. Cada verbo tem uma constante associada a ele para identificação, definida no EXCHFORM. Arquivo de header H. A tabela a seguir lista os verbos de formulário padrão e suas constantes associadas:
  
|**Verb**|**Valor**|
|:-----|:-----|
|Abrir  <br/> |EXCHIVERB_OPEN  <br/> |
|Responder  <br/> |EXCHIVERB_REPLYTOSENDER  <br/> |
|Responder a Todos  <br/> |EXCHIVERB_REPLYTOALL  <br/> |
|Encaminhar  <br/> |EXCHIVERB_FORWARD  <br/> |
|Imprimir  <br/> |EXCHIVERB_PRINT  <br/> |
|Salvar como  <br/> |EXCHIVERB_SAVEAS  <br/> |
|Responder para Pasta  <br/> |EXCHIVERB_REPLYTOFOLDER  <br/> |
   
Quando um usuário escolher um verbo, passe sua constante em uma chamada para o método [IMAPIForm::D oVerb](imapiform-doverb.md) do formulário para executar sua ação correspondente. 
  
Além de acessar verbos por meio do visualizador de formulário, os usuários podem, às vezes, acessar verbos diretamente do formulário. For example, some form objects allow the user to invoke the Print verb by **right-clicking** on the form and choosing **Print** from a context-sensitive menu. 
  

