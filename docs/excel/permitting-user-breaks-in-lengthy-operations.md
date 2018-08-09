---
title: Permitir intervenções de usuário em operações demoradas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- função xlAbort [excel 2007], tarefas simultâneas [Excel 2007], quebras de usuário [Excel 2007]
localization_priority: Normal
ms.assetid: 0e3df597-0aa6-497f-bc52-58c7dc064538
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: b13f9b9a8c0e5621b25df13537632bdbe5dfc29e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765427"
---
# <a name="permitting-user-breaks-in-lengthy-operations"></a>Permitir intervenções de usuário em operações demoradas

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Embora o Windows usa preventivo multitarefa, onde suas funções ou comandos podem levar muito tempo para executar, é uma boa prática para gerar algum tempo para o sistema operacional agora e novamente para ajudá-lo a agendar tarefas simultâneas. Usando as chamadas nativas do Windows, você pode fazer isso usando a função de suspensão. Usando a API C, você pode executá-la usando a [função xlAbort](xlabort.md), que não só produz o processador para uma instantânea, mas também verifica se o usuário pressiona a tecla de cancelar, **ESC**.
  
A função **xlAbort** , portanto, permite que o seu código para verificar se o usuário deseja finalizar o processo, faça a limpeza necessária e devolver o controle para o Excel. A função também permite que você limpar a condição de quebra. Isso permite que seus comandos exibir uma caixa de diálogo para verificar se o usuário deseja finalizar o comando. Se não quiser que o usuário encerrar o comando, chamar a função **xlAbort** com o argumento *FALSE* limpa a quebra. (O argumento padrão é *TRUE* , o que simplesmente verifica a condição, mas não desmarcou.) 
  
Você pode chamar a função **xlAbort** a partir de uma função definida pelo usuário (UDF) ou um comando XLL. Em um UDF, quando a função **xlAbort** retorna **TRUE**, tendo detectada uma quebra de usuário, você faria normalmente cortar curto cálculo da função e retornar algum valor para indicar que o cálculo não foi concluída, talvez qualquer erro ou zero. Desmarque a condição de quebra não para que outras instâncias de funções longas que também verificam essa condição também serão desfeitos. Excel implicitamente limpa essa condição quando um recálculo for encerrada.
  
Quando você detectar uma condição de quebra em um comando, você geralmente desmarcar a condição chamando a função **xlAbort** novamente com o argumento **Falso**, embora Excel implicitamente limpa essa condição quando um comando for encerrada.
  
## <a name="see-also"></a>Confira também



[Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Recálculo do vários threads no Excel](multithreaded-recalculation-in-excel.md)
  
[Desenvolvimento de XLLs do Excel](developing-excel-xlls.md)
  
[Acessar a instância do Excel e as alças da janela principal](how-to-access-excel-instance-and-main-window-handles.md)

