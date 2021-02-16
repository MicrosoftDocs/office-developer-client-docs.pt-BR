---
title: Solucionar problemas de modelos de formulário que usam o modelo de objeto do InfoPath em tempo de design
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- modelos de formulário compatíveis com infopath 2003, solução de problemas em tempo de design, solução de problemas de modelos de formulário [InfoPath 2007], tempo de design
localization_priority: Normal
ms.assetid: 4179b235-e21d-4c37-ae2b-ad01388296ec
description: As seções a seguir descrevem cenários comuns de solução de problemas que você pode encontrar durante a criação e depuração de modelos de formulário de código gerenciado que usam o modelo de objeto compatível com o InfoPath 2003 fornecido pelo namespace Microsoft.Office.Interop.InfoPath.SemiTrust.
ms.openlocfilehash: 106f12602bae86d85c2a7d2f920f59d50326c908
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436521"
---
# <a name="troubleshoot-form-templates-that-use-the-infopath-object-model-at-design-time"></a>Solucionar problemas de modelos de formulário que usam o modelo de objeto do InfoPath em tempo de design

As seções a seguir descrevem cenários comuns de solução de problemas que você pode encontrar durante a criação e depuração de modelos de formulário de código gerenciado que usam o modelo de objeto compatível com o InfoPath 2003 fornecido pelo namespace **Microsoft.Office.Interop.InfoPath.SemiTrust.** 
  
## <a name="cannot-preview-or-debug-form-templates-that-use-calls-to-object-model-security-level-3-methods-and-properties"></a>Não é possível visualizar ou depurar modelos de formulário que usam métodos e propriedades de nível 3 de segurança de chamadas para o modelo de objeto

Se você tentar depurar ou visualizar um projeto de código gerenciado que contenha código que invoque membros do modelo de objeto que exigem confiança total, o InfoPath exibirá a mensagem de erro "Ocorreu uma exceção de segurança sem tratamento no código do formulário" e o formulário não será aberto. Para permitir que a lógica de negócios no modelo de formulário seja  depurada ou visualizada, você deve definir o nível de segurança como Confiança Total e assinar digitalmente o modelo de formulário. Para obter detalhes sobre como fazer isso, consulte Visualizar e depurar modelos de formulário [que exigem confiança total.](how-to-preview-and-debug-form-templates-that-require-full-trust.md)
  
## <a name="cannot-update-xpath-expressions-in-event-handlers-if-the-matchpath-parameter-value-was-deleted-manually"></a>Não é possível atualizar expressões XPath em manipuladores de eventos se o valor do parâmetro MatchPath foi excluído manualmente

Se você adicionar um manipulador de eventos a um campo ou grupo e alterar posteriormente o esquema da fonte de dados no painel de tarefas Campos do **InfoPath** de uma maneira que afete esse campo ou grupo (por exemplo, renomeando ou movendo-o), uma mensagem será exibida perguntando se você deseja atualizar as expressões XPath no código do seu formulário. As expressões XPath mencionadas nesta mensagem são os valores especificados no parâmetro [MatchPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) do atributo [InfoPathEventHandlerAttribute,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) que são usados para associar o manipulador de eventos a um campo ou grupo na fonte de dados do formulário. Nenhuma outra expressão XPath em seu código será atualizada. O algoritmo para atualizar as expressões XPath depende de um valor presente no parâmetro **MatchPath** dos atributos **do InfoPathEventHandler** aplicados no código do formulário. Se você excluiu manualmente esses valores antes de responder ao prompt para atualizar expressões XPath, o InfoPath não poderá atualizar as expressões XPath automaticamente. Para obter mais informações, consulte Adicionar um manipulador de eventos usando o modelo de objeto do [InfoPath 2003.](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)
  
## <a name="cannot-call-members-of-the-infopath-2003-compatible-object-model-on-a-separate-thread"></a>Não é possível chamar membros do modelo de objeto compatível com o InfoPath 2003 em um thread separado

O modelo de objeto compatível com o InfoPath 2003 não dá suporte a chamadas em um thread separado. Por exemplo, o código a seguir, que chama uma função chamada LaunchOMFunction que chama membros do modelo de objeto do InfoPath, não será executado. 
  
```cs
Thread th = new Thread(new ThreadStart(LaunchOMFunction));
th.Start();
```

Quando necessário, há uma maneira de resolver essa limitação. Para obter informações, consulte Suporte a threading em projetos do InfoPath usando o modelo de objeto [do InfoPath 2003.](threading-support-in-infopath-projects-using-the-infopath-2003-object-model.md)
  
## <a name="omitting-optional-parameters-causes-a-build-error-in-visual-basic-and-visual-c"></a>Omitir parâmetros opcionais causa um erro de com build no Visual Basic e no Visual C #

Se um membro do modelo de objeto do InfoPath contiver um parâmetro opcional e você não especificar um valor para esse parâmetro, deverá passar o campo **Type.Missing** para esse parâmetro. Não transferir o campo **Type.Missing** quando um valor real for omitido resultará em um erro de compilação. Isso é verdadeiro para código escrito no Visual Basic e no Visual C#. Para obter mais informações e exemplos, consulte a seção "Passando parâmetros opcionais para membros do modelo de objeto do InfoPath" no tópico Modelos de objeto compatíveis com [o InfoPath 2003.](infopath-2003-compatible-object-models.md) 
  
## <a name="see-also"></a>Confira também

- [Sobre o modelo de segurança para modelos de formulário com código](about-the-security-model-for-form-templates-with-code.md)
- [Implantar modelos de formulário do InfoPath com código](how-to-deploy-infopath-form-templates-with-code.md)
- [Tratar erros usando o modelo de objeto do InfoPath 2003](how-to-handle-errors-using-the-infopath-2003-object-model.md)
- [Visualizar e depurar modelos de formulário que exigem confiança total](how-to-preview-and-debug-form-templates-that-require-full-trust.md)
- [Depurar projetos do InfoPath usando o modelo de objeto do InfoPath 2003](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)

