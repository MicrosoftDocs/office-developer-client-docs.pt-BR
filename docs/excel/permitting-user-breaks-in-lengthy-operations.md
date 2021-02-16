---
title: Permitir quebras de usuário em operações demoradas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- função xlabort [excel 2007],tarefas simultâneas [Excel 2007],quebras de usuário [Excel 2007]
localization_priority: Normal
ms.assetid: 0e3df597-0aa6-497f-bc52-58c7dc064538
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 650af14e4e97ebd2642a4442a87965f313d3b556
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414687"
---
# <a name="permitting-user-breaks-in-lengthy-operations"></a>Permitir quebras de usuário em operações demoradas

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Embora o Windows use multitarefa preventiva, onde suas funções ou comandos podem levar muito tempo para ser executado, é uma boa prática gerar algum tempo para o sistema operacional agora e novamente para ajudá-lo a agendar tarefas simultâneas. Usando chamadas nativas do Windows, você pode fazer isso usando a função de sleep. Usando a API de C, você pode fazer isso usando a função [xlAbort](xlabort.md), que não só produz o processador por um instantâneo, mas também verifica se o usuário pressionou a tecla de cancelamento, **ESC**.
  
A **função xlAbort,** portanto, permite que seu código verifique se o usuário deseja finalizar o processo, fazer a limpeza necessária e retornar o controle para o Excel. A função também permite limpar a condição de quebra. Isso permite que seus comandos exibem uma caixa de diálogo para verificar se o usuário deseja finalizar o comando. Se o usuário não quiser finalizar o comando, chamar a função **xlAbort** com o argumento  *FALSE*  limpará a pausa. (O argumento padrão é  *TRUE*  , que simplesmente verifica a condição, mas não a limpa.) 
  
Você pode chamar a **função xlAbort** a partir de uma função definida pelo usuário (UDF) ou de um comando XLL. Em uma UDF, quando a função **xlAbort** retorna **VERDADEIRO**, após detectar uma quebra de usuário, você normalmente cortaria o cálculo da função e retornaria algum valor para indicar que o cálculo não foi concluído, talvez um erro ou zero. Você não limparia a condição de quebra para que outras instâncias de funções longas que também verificam essa condição também quebram. O Excel limpa implicitamente essa condição quando um recálculo termina.
  
When you detect a break condition in a command, you typically clear the condition by calling the **xlAbort** function again with the argument **FALSE**, although Excel implicitly clears this condition when a command ends.
  
## <a name="see-also"></a>Confira também



[Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Recálculo com vários threads no Excel](multithreaded-recalculation-in-excel.md)
  
[Desenvolvimento de XLLs do Excel](developing-excel-xlls.md)
  
[Acessar a instância do Excel e as alças da janela principal](how-to-access-excel-instance-and-main-window-handles.md)

