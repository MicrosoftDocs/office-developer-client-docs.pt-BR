---
title: Implementar verbos de formulário padrão
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8135af7947f30ac600b8d9af364b2a79a3443ab6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767446"
---
# <a name="implementing-standard-form-verbs"></a>Implementar verbos de formulário padrão

  
  
**Aplica-se a**: Outlook 
  
MAPI define um conjunto de verbos padrão ou ações tomadas quando um usuário faz uma seleção de menu ou clicar em um botão, que devem oferecer suporte a todos os visualizadores de formulário. Cada verbo tem uma constante associada a ela para identificação, definida no EXCHFORM. Arquivo de cabeçalho H. A tabela a seguir lista os verbos formulário padrão e suas constantes associados:
  
|**Verbo**|**Valor**|
|:-----|:-----|
|Abrir  <br/> |EXCHIVERB_OPEN  <br/> |
|Responder  <br/> |EXCHIVERB_REPLYTOSENDER  <br/> |
|Responder a Todos  <br/> |EXCHIVERB_REPLYTOALL  <br/> |
|Encaminhar  <br/> |EXCHIVERB_FORWARD  <br/> |
|Imprimir  <br/> |EXCHIVERB_PRINT  <br/> |
|Salvar como  <br/> |EXCHIVERB_SAVEAS  <br/> |
|Responder para Pasta  <br/> |EXCHIVERB_REPLYTOFOLDER  <br/> |
   
Quando o usuário escolhe um verbo, passe sua constante em uma chamada ao método de [IMAPIForm::DoVerb](imapiform-doverb.md) do formulário para executar sua ação correspondente. 
  
Além das acessando verbos através de sua tela de formulário, às vezes, os usuários podem acessar o verbos diretamente do formulário. Por exemplo, alguns objetos de formulário permitem que o usuário invocar o verbo **Imprimir** clicando duas vezes no formulário e escolhendo a **impressão** de um menu sensível ao contexto. 
  

