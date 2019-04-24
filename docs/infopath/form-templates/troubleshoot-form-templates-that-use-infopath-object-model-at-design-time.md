---
title: Solucionar problemas de modelos de formulário que usam o modelo de objeto do InfoPath no tempo de design
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- modelos de formulário compatíveis com o InfoPath 2003, Solucionando problemas no tempo de design, Solucionando problemas de modelos de formulário [InfoPath 2007], tempo de design
localization_priority: Normal
ms.assetid: 4179b235-e21d-4c37-ae2b-ad01388296ec
description: As seções a seguir descrevem cenários de solução de problemas comuns que você pode encontrar ao criar e depurar modelos de formulário de código gerenciado que usam o modelo de objeto compatível com o InfoPath 2003 fornecido pelo Microsoft. Office. Interop. InfoPath. SemiTrust namespace.
ms.openlocfilehash: 106f12602bae86d85c2a7d2f920f59d50326c908
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303469"
---
# <a name="troubleshoot-form-templates-that-use-the-infopath-object-model-at-design-time"></a>Solucionar problemas de modelos de formulário que usam o modelo de objeto do InfoPath no tempo de design

As seções a seguir descrevem cenários de solução de problemas comuns que você pode encontrar ao criar e depurar modelos de formulário de código gerenciado que usam o modelo de objeto compatível com o InfoPath 2003 fornecido pelo ** Namespace Microsoft. Office. Interop. InfoPath. SemiTrust** . 
  
## <a name="cannot-preview-or-debug-form-templates-that-use-calls-to-object-model-security-level-3-methods-and-properties"></a>Não é possível visualizar ou depurar modelos de formulário que usam chamadas para métodos de segurança do modelo de objeto 3 e propriedades

Se você tentar depurar ou Visualizar um projeto de código gerenciado que contenha código que invoque membros de modelo de objeto que exigem confiança total, o InfoPath exibirá a mensagem de erro "ocorreu uma exceção de segurança sem tratamento no código do formulário" e o formulário não será aberto . Para permitir que a lógica de negócios no modelo de formulário seja depurada ou visualizada, você deve definir o nível de segurança como **confiança total** e assinar digitalmente o modelo de formulário. Para obter detalhes sobre como fazer isso, confira [Visualizar e depurar modelos de formulário que exigem confiança total](how-to-preview-and-debug-form-templates-that-require-full-trust.md).
  
## <a name="cannot-update-xpath-expressions-in-event-handlers-if-the-matchpath-parameter-value-was-deleted-manually"></a>Não é possível atualizar expressões XPath em manipuladores de eventos se o valor do parâmetro MatchPath tiver sido excluído manualmente

Se você adicionar um manipulador de eventos a um campo ou grupo e posteriormente alterar o esquema da fonte de dados no painel de tarefas **campos** do InfoPath de uma maneira que afete esse campo ou grupo (por exemplo, renomeando ou movendo-o), uma mensagem será exibida perguntando se você deseja atualizar e as expressões XPath no código do seu formulário. As expressões XPath referenciadas nesta mensagem são os valores especificados no parâmetro [MatchPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) do atributo [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) , que são usados para associar o manipulador de eventos a um campo ou grupo na fonte de dados do formulário . Nenhuma outra expressão XPath no seu código será atualizada. O algoritmo para atualizar as expressões XPath depende de um valor presente no parâmetro **MatchPath** dos atributos **InfoPathEventHandler** que são aplicados no seu código de formulário. Se você excluiu manualmente esses valores antes de responder ao prompt para atualizar expressões XPath, o InfoPath não poderá atualizar as expressões XPath automaticamente. Para obter mais informações, consulte [Adicionar um manipulador de eventos usando o modelo de objeto do InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).
  
## <a name="cannot-call-members-of-the-infopath-2003-compatible-object-model-on-a-separate-thread"></a>Não é possível chamar membros do modelo de objeto compatível com o InfoPath 2003 em um thread separado

O modelo de objeto compatível com o InfoPath 2003 não oferece suporte a chamadas em um thread separado. Por exemplo, o código a seguir, que chama uma função chamada LaunchOMFunction que chama membros do modelo de objeto do InfoPath, não será executado. 
  
```cs
Thread th = new Thread(new ThreadStart(LaunchOMFunction));
th.Start();
```

Quando necessário, há uma forma de contornar essa limitação. Para saber mais, confira [suporte a Threading em projetos do InfoPath usando o modelo de objeto do infopath 2003](threading-support-in-infopath-projects-using-the-infopath-2003-object-model.md).
  
## <a name="omitting-optional-parameters-causes-a-build-error-in-visual-basic-and-visual-c"></a>A omissão de parâmetros opcionais causa um erro de compilação no Visual Basic e no Visual C#

Se um membro do modelo de objeto do InfoPath contiver um parâmetro opcional e você não especificar um valor para esse parâmetro, você deverá passar o **tipo. campo ausente** para esse parâmetro. Não transferir o campo **Type.Missing** quando um valor real for omitido resultará em um erro de compilação. Isso se aplica ao código escrito em Visual Basic e Visual C#. Para obter mais informações e exemplos, consulte a seção "passando parâmetros opcionais para membros do modelo de objeto do InfoPath" no tópico [modelos de objeto compatíveis com o infopath 2003](infopath-2003-compatible-object-models.md) . 
  
## <a name="see-also"></a>Confira também

- [Sobre o modelo de segurança para modelos de formulário com código](about-the-security-model-for-form-templates-with-code.md)
- [Implantar modelos de formulário do InfoPath com código](how-to-deploy-infopath-form-templates-with-code.md)
- [Manipular erros usando o modelo de objeto do InfoPath 2003](how-to-handle-errors-using-the-infopath-2003-object-model.md)
- [Visualizar e depurar modelos de formulário que exigem confiança total](how-to-preview-and-debug-form-templates-that-require-full-trust.md)
- [Depurar projetos do InfoPath usando o modelo de objeto do InfoPath 2003](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)

