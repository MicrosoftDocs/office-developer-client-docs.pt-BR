---
title: Acessar o código de XLL no Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- acesso ao código de xll [excel 2007],XLLs [Excel 2007], acesso ao código,comandos [Excel 2007], registro,funções [Excel 2007], registro,chamar XLLs a partir do Excel,registrar comandos [Excel 2007],registrar funções [Excel 2007]
ms.assetid: 6e4bf1f3-8eca-4be5-9632-75355ac31d61
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: d1332b0dffc052404c75c4ec51d94879457c3da0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304183"
---
# <a name="accessing-xll-code-in-excel"></a>Acessar o código de XLL no Excel

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Para ficar acessível no Microsoft Excel, as funções e os comandos que um XLL contém:
  
- Devem ser exportados pelo XLL.
    
- Devem estar registrados no Excel.
    
## <a name="registering-functions-and-commands-with-excel"></a>Como registrar comandos e funções no Excel

O registro informa o seguinte ao Excel sobre um ponto de entrada DLL:
  
- Se está oculto ou, no caso de uma função, se está visível no Assistente de Função.
    
- Se pode ser chamado somente de uma folha de macro XLM ou também de uma planilha.
    
- Quando é um comando, se é uma função de planilha ou uma função equivalente da folha de macro.
    
- O que é o nome de exportação de XLL/DLL e qual nome deseja que o Excel use.
    
- Quando é uma função:
    
  - Quais tipos de dados ela retorna e recebe como argumentos.
    
  - Se retorna o resultado modificando um argumento em vigor.
    
  - Se é volátil.
    
  - Se é isento de threads (com suporte a partir do Excel 2007).
    
  - Que texto o Assistente de função Colar e o editor de AutoCompletar devem exibir para ajudar a chamar a função.
    
  - Qual categoria de função deveria ser listada.
    
Tudo isso é obtido usando a função da API C [xlfRegister](xlfregister-form-1.md), equivalente à função XLM **REGISTER**.
  
## <a name="calling-xll-functions-directly-from-excel"></a>Como chamar funções de DLL diretamente do Excel

Após serem registradas, as funções de planilha e planilha de macro XLL podem ser chamadas de qualquer lugar em que uma função interna possa ser chamada:
  
- Uma fórmula de célula única ou matriz em uma planilha.
    
- Uma fórmula de célula única ou matriz em uma planilha de macro.
    
- A definição de um nome definido.
    
- Os campos de condição e limite em uma caixa de diálogo de formato condicional.
    
- De outro suplemento por meio da função da API C [xlUDF](xludf.md).
    
- Do Visual Basic for Applications (VBA) por meio do método **Application.Run**. 
    
Você pode obter uma referência à célula de chamada ou ao intervalo de células dentro de sua função usando a função da API C **xlfCaller**. Se a função foi chamada da expressão de formato condicional da célula, ainda será retornada uma referência à célula ou células associadas, portanto, não é possível presumir que a fórmula da célula contenha a função de XLL. Se sua função foi chamada de uma função definida pelo usuário do VBA (UDF), **xlfCaller** retorna novamente o endereço das células que chamaram a função VBA. Para saber mais, confira [xlfCaller](xlfcaller.md).
  
> [!NOTE]
> O Excel também chama funções de XLL no **Assistente de Função Colar** e caixas de diálogo **Substituir**. Pode ser necessário restringir a execução normal de seu código no caso da caixa de diálogo **Argumentos da Função Colar**, especialmente onde sua função pode levar muito tempo para ser executada. Para detectar se sua função está sendo chamada de qualquer uma dessas caixas de diálogo, implemente código em seu projeto para percorrer todas as janelas abertas para determinar se a janela frontal é uma dessas caixas de diálogo e, em caso afirmativo, qual delas. 
  
## <a name="calling-xll-commands-directly-from-excel"></a>Como chamar comandos de XLL diretamente do Excel

Uma vez registrados, os comandos de XLL podem ser chamados de todas as maneiras que outras macros definidas pelo usuário podem ser chamadas:
  
- Por estarem associados a um objeto de controle incorporado a uma planilha.
    
- Na caixa de diálogo Executar Macro.
    
- De uma macro definida pelo usuário do VBA usando o método **Application.Run**. 
    
- De uma barra de ferramentas ou item de menu personalizado.
    
- Usar um pressionamento de tecla de atalho configurado ao registrar o comando.
    
- Como o comando a ser executado quando um evento especificado é interceptado.
    
> [!NOTE]
> Os comandos de XLL estão ocultos porque não aparecem na lista de macros disponíveis nas caixas de diálogo do Excel. No entanto, podem ser inseridos manualmente no campo de nome da macro. O Excel espera o nome registrado como está nessas caixas de diálogo, não o nome de exportação de DLL. 
  
Todos os comandos de XLL registrados com o Excel são considerados pelo Excel da forma a seguir:
  
```cs
short WINAPI xll_cmd_name(void)
{
// Function code...
    return 1;
}

```

O Excel ignora o valor de retorno, a menos que ele seja chamado de uma planilha de macro XLM; neste caso, o valor de retorno é convertido para **TRUE** ou **FALSE**. Portanto, você deve retornar 1 se o comando foi executado com sucesso e 0 se falhou ou foi cancelado pelo usuário.
  
Você pode obter informações sobre a forma como o comando foi invocado usando a função da API C **xlfCaller**. Para saber mais, confira [xlfCaller](xlfcaller.md).
  
Iniciar na interface do usuário do Excel 2007 é muito diferente das versões anteriores. As funções da API C que permitem a adição e exclusão de barras de menus personalizadas, menus, submenus, itens de menu, barras de ferramentas personalizadas e botões da barra de ferramentas ainda têm suporte na maioria dos casos. No entanto, elas nem sempre disponibilizam o item adicionado na forma que os usuários já conhecem. Você deve verificar cuidadosamente se alguma funcionalidade adicional ainda está acessível ou implementar uma personalização específica da versão. A partir do Excel 2007, a interface do usuário é personalizada de forma mais eficaz usando um módulo de código gerenciado que pode ser fortemente acoplado aos comandos de XLL.
  
## <a name="see-also"></a>Confira também

- [Como criar XLLs](creating-xlls.md)
- [Chamar funções de XLL no Assistente de Função ou nas caixas de diálogo Substituir](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
- [Gerenciador de Suplemento e Funções da Interface XLL](add-in-manager-and-xll-interface-functions.md)
- [Desenvolvimento de XLLs do Excel](developing-excel-xlls.md)



