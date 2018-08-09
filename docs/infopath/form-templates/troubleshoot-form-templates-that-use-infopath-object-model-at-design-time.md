---
title: Solucionar problemas de modelos de formulário que usam o modelo de objeto do InfoPath em tempo de design
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- tempo de design de modelos de formulário de 2003 compatíveis do InfoPath, solução de problemas em tempo de design, solucionando problemas de modelos de formulário [InfoPath 2007]
localization_priority: Normal
ms.assetid: 4179b235-e21d-4c37-ae2b-ad01388296ec
description: As próximas seções descrevem os cenários de solução de problemas comuns, que você pode encontrar durante a criação e depuração de modelos de formulário de código gerenciado que usam o modelo de objeto compatível com o InfoPath 2003 fornecido pelo SemiTrust namespace.
ms.openlocfilehash: af71c8058744561a4c8ee0870fb37054e9979751
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765708"
---
# <a name="troubleshoot-form-templates-that-use-the-infopath-object-model-at-design-time"></a>Solucionar problemas de modelos de formulário que usam o modelo de objeto do InfoPath em tempo de design

As próximas seções descrevem os cenários de solução de problemas comuns, que você pode encontrar durante a criação e depuração de modelos de formulário de código gerenciado que usam o modelo de objeto compatível com o InfoPath 2003 fornecido pelo ** SemiTrust** namespace. 
  
## <a name="cannot-preview-or-debug-form-templates-that-use-calls-to-object-model-security-level-3-methods-and-properties"></a>Não é possível visualizar ou modelos de formulário de depuração que usam chamadas para o objeto modelar propriedades e métodos de nível 3 de segurança

Se você tentar depurar ou preview confiar em um projeto de código gerenciado que contém código que chama os membros do modelo de objeto que exigem completa, InfoPath exibirá a mensagem de erro "Ocorreu uma exceção de segurança não tratada no código do formulário" e o formulário não será aberto. . Para permitir que a lógica de negócios no modelo de formulário a ser depurados ou visualizados, você deve definir o nível de segurança como **Confiança total** e assinar digitalmente o modelo de formulário. Para obter detalhes sobre como fazer isso, consulte [Visualizar e depurar modelos de formulário que exigem confiança total](how-to-preview-and-debug-form-templates-that-require-full-trust.md).
  
## <a name="cannot-update-xpath-expressions-in-event-handlers-if-the-matchpath-parameter-value-was-deleted-manually"></a>Não é possível atualizar as expressões XPath nos manipuladores de eventos, se o valor do parâmetro MatchPath foi excluído manualmente

Se você adiciona um manipulador de eventos a um campo ou grupo e posteriormente alterar o esquema da fonte de dados no painel de tarefas do InfoPath **campos** de uma forma que afeta esse campo ou grupo (por exemplo, por renomeando ou movendo-), uma mensagem será exibida perguntando se você deseja atualiza f o XPath expressões em código do formulário. As expressões XPath referidas nessa mensagem são os valores especificados no parâmetro [MatchPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) do atributo [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) , que são usados para associar o manipulador de eventos um campo ou grupo na fonte de dados do formulário . Não há outras expressões XPath em seu código serão atualizados. O algoritmo para atualizar as expressões XPath depende de um valor que está sendo presente no parâmetro **MatchPath** dos atributos **InfoPathEventHandler** que são aplicados em seu código de formulário. Se você excluiu manualmente esses valores antes de responder ao prompt para atualizar as expressões XPath, o InfoPath não poderá atualizar as expressões XPath automaticamente. Para obter mais informações, consulte [Adicionar um manipulador de eventos usando o modelo de objeto do InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).
  
## <a name="cannot-call-members-of-the-infopath-2003-compatible-object-model-on-a-separate-thread"></a>Não é possível chamar membros do modelo de objeto do InfoPath 2003 compatível com em um segmento separado

O modelo de objeto compatível com o InfoPath 2003 não oferece suporte a chamadas em um segmento separado. Por exemplo, o código a seguir, que chama uma função chamada LaunchOMFunction que chama os membros do modelo de objeto do InfoPath, não será executado. 
  
```cs
Thread th = new Thread(new ThreadStart(LaunchOMFunction));
th.Start();
```

Quando necessário, há uma maneira para contornar esta limitação. Para obter informações, consulte [Suporte Threading InfoPath projetos usando o modelo de objeto do InfoPath 2003](threading-support-in-infopath-projects-using-the-infopath-2003-object-model.md).
  
## <a name="omitting-optional-parameters-causes-a-build-error-in-visual-basic-and-visual-c"></a>Omitir os parâmetros opcionais causará um erro de compilação no Visual Basic e Visual c#

Se um membro de modelo de objeto do InfoPath contém um parâmetro opcional e você não especificar um valor para esse parâmetro, você deve passar o campo **Type.Missing** para esse parâmetro em vez disso. Falha ao passar o campo **Type.Missing** quando um valor real for omitido resultará em um erro de compilação. Isso é verdadeiro para códigos escritos em Visual Basic e Visual c#. Para obter mais informações e exemplos, consulte a seção "Passando opcional para InfoPath modelo membros do objeto Parameters" no tópico [Modelos de objeto do InfoPath 2003 compatíveis](infopath-2003-compatible-object-models.md) . 
  
## <a name="see-also"></a>Confira também

- [Sobre o modelo de segurança para modelos de formulário com código](about-the-security-model-for-form-templates-with-code.md)
- [Implantar modelos de formulário do InfoPath com código](how-to-deploy-infopath-form-templates-with-code.md)
- [Lidar com erros usando o modelo de objeto do InfoPath 2003](how-to-handle-errors-using-the-infopath-2003-object-model.md)
- [Visualizar e depurar modelos de formulário que exigem confiança total](how-to-preview-and-debug-form-templates-that-require-full-trust.md)
- [Depurar projetos do InfoPath usando o modelo de objeto do InfoPath 2003](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)

