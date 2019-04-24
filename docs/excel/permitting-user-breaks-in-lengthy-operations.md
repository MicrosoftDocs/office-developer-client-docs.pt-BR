---
title: Permitir quebras de usuário em operações deMoradas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- função xlAbort [Excel 2007], tarefas simultâneas [Excel 2007], o usuário quebra [Excel 2007]
localization_priority: Normal
ms.assetid: 0e3df597-0aa6-497f-bc52-58c7dc064538
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 650af14e4e97ebd2642a4442a87965f313d3b556
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310378"
---
# <a name="permitting-user-breaks-in-lengthy-operations"></a>Permitir quebras de usuário em operações deMoradas

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Embora o Windows Use multitarefas preemptivas, onde suas funções ou comandos podem levar muito tempo para serem executados, é uma boa prática levar algum tempo para o sistema operacional agora e novamente para ajudá-lo a agendar tarefas simultâneas. Usando chamadas nativas do Windows, você pode fazer isso usando a função Sleep. Usando a API C, você pode fazer isso usando a [função xlAbort](xlabort.md), que não só produz o processador para um instante, mas também verifica se o usuário pressionou a tecla Cancelar, **ESC**.
  
Portanto, a função **xlAbort** permite que o código Verifique se o usuário deseja finalizar o processo, faça a limpeza necessária e, em seguida, retorne o controle para o Excel. A função também permite que você desmarque a condição de interrupção. Isso permite que os comandos exibam uma caixa de diálogo para verificar se o usuário deseja encerrar o comando. Se o usuário não quiser encerrar o comando, chamar a função **xlAbort** com o argumento *false* desmarcará a quebra. (O argumento padrão é *true* , que simplesmente verifica a condição, mas não a limpa.) 
  
Você pode chamar a função **xlAbort** de uma função definida pelo usuário (UDF) ou de um comando XLL. Em um UDF, quando a função **xlAbort** retorna **true**, tendo detectado uma quebra de usuário, você normalmente recortou curto o cálculo da função e retorna um valor para indicar que o cálculo não foi concluído, talvez um erro ou zero. Você não desmarcaria a condição de interrupção para que outras instâncias de funções demoradas também marquem esta condição também sejam interrompidas. O Excel desmarca implicitamente essa condição quando um recálculo termina.
  
Quando você detecta uma condição de interrupção em um comando, normalmente limpa a condição chamando a função **xlAbort** novamente com o argumento **false**, embora o Excel desmarque implicitamente essa condição quando um comando termina.
  
## <a name="see-also"></a>Confira também



[Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Recálculo com vários threads no Excel](multithreaded-recalculation-in-excel.md)
  
[Desenvolvimento de XLLs do Excel](developing-excel-xlls.md)
  
[Acessar a instância do Excel e as alças da janela principal](how-to-access-excel-instance-and-main-window-handles.md)

