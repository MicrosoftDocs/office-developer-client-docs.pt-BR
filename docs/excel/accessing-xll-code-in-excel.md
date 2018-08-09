---
title: Acessando código XLL no Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- acessando código xll [excel 2007], XLLs [Excel 2007], acessando código, comandos [Excel 2007], registro, funções [Excel 2007], registro, chamando XLLs do Excel, registrando comandos [Excel 2007], registrando funções [Excel 2007]
localization_priority: Normal
ms.assetid: 6e4bf1f3-8eca-4be5-9632-75355ac31d61
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1523f9e8213cb955f1bfd995c42f921b001299fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765260"
---
# <a name="accessing-xll-code-in-excel"></a>Acessando código XLL no Excel

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Seja acessível no Microsoft Excel, as funções e comandos que contém um XLL:
  
- Deve ser exportados pelo XLL.
    
- Deve ser registrado com o Excel.
    
## <a name="registering-functions-and-commands-with-excel"></a>Registrando as funções e comandos com o Excel

Registro informa Excel a seguir sobre um ponto de entrada DLL:
  
- Se ele estiver oculto ou se uma função, se ele estiver visível no Assistente de função.
    
- Se ele está acessível somente a partir de uma folha de macro XLM ou também uma planilha.
    
- Se um comando, se é uma função de planilha ou uma função equivalente de folha de macro.
    
- Qual é o seu nome de exportação XLL/DLL e que nome que você deseja que o Excel use.
    
- Se ele é uma função:
    
  - Quais dados retorna as digita e utiliza como argumentos.
    
  - Se ela retorna seu resultado modificando um argumento in-loco.
    
  - Se ele está voláteis.
    
  - Se ele está thread-safe (começando com suporte no Excel 2007).
    
  - O que o Assistente de função colar de texto e o editor de AutoCompletar devem ser exibida para ajudá-lo com chamar a função.
    
  - Qual funcionar categoria, em que ele deve estar listado.
    
Tudo isso é obtido usando a API C função [xlfRegister](xlfregister-form-1.md), equivalente à função XLM **registrar**.
  
## <a name="calling-xll-functions-directly-from-excel"></a>Chamando funções XLL diretamente do Excel

Depois que eles são registrados, as funções de folha de macro e de planilha XLL podem ser chamadas em qualquer lugar, de que uma função incorporada pode ser chamada:
  
- Uma fórmula de célula única ou matriz em uma planilha.
    
- Uma fórmula de célula única ou matriz em uma folha de macro.
    
- A definição de um nome definido.
    
- Os campos de condição e limite em uma caixa de diálogo formato condicional.
    
- De outro suplemento por meio da API C funcione [xlUDF](xludf.md).
    
- No Visual Basic for Applications (VBA) por meio do método **Run** . 
    
Você pode obter uma referência para a célula ou intervalo de células de chamada dentro de sua função usando a função do C API **xlfCaller**. Se a função foi chamada de expressão de formatação condicional da célula, você ainda retorna uma referência para a célula associada ou células, portanto você não pode assumir que a fórmula da célula contém a função XLL. Se a sua função foi chamada a partir de uma função definida pelo usuário do VBA (UDF), o **xlfCaller** novamente devolve o endereço das células que a chamada de função do VBA. Para obter mais informações, consulte [xlfCaller](xlfcaller.md).
  
> [!NOTE]
> Excel também chama o código de função XLL de caixas de diálogo **Assistente de função colar** e **Substituir** . Talvez seja necessário restringir seu código normal em execução no caso da caixa de diálogo **Argumentos da função colar** , especialmente onde sua função pode levar muito tempo para executar. Para detectar se a sua função está sendo chamada de qualquer um dessas caixas de diálogo, você deve implementar alguns códigos em seu projeto que itera todas as janelas abertas para determinar se a janela front é uma dessas caixas de diálogo e, em caso afirmativo, qual deles. 
  
## <a name="calling-xll-commands-directly-from-excel"></a>Chamar comandos XLL diretamente do Excel

Depois que eles são registrados, comandos XLL podem ser chamados em todas as formas que outras macros definidas pelo usuário podem ser chamadas:
  
- Por sendo associado a um objeto control incorporadas em uma planilha.
    
- Na caixa de diálogo Executar Macro.
    
- De uma macro VBA definidas pelo usuário, usando o método Application **Run** . 
    
- A partir de um item de menu personalizado ou uma barra de ferramentas.
    
- Usando um pressionamento de tecla de atalho configurar ao registrar o comando.
    
- Como o comando a ser executado quando um evento específico é interceptado.
    
> [!NOTE]
> Comandos XLL estão ocultos em que eles não apareçam na lista de macros disponíveis nas caixas de diálogo do Excel. Mas podem ser inseridos manualmente no campo nome da macro. Excel espera que o nome registrado como essas caixas de diálogo, não o nome da DLL export. 
  
Todos os comandos XLL registrados com o Excel diferenciam pelo Excel deve estar no seguinte formato:
  
```cs
short WINAPI xll_cmd_name(void)
{
// Function code...
    return 1;
}

```

[!OBSERVA��O] O Excel ignorar� o valor de retorno, a menos que ele seja chamado de uma folha de macros XLM; nesse caso, o valor de retorno ser� convertido em **TRUE** ou em **FALSE**. Dessa forma, voc� dever� retornar 1 se o seu comando tiver sido executado com �xito e 0 caso ele tenha falhado ou tenha sido cancelado pelo usu�rio.
  
Você pode obter informações sobre como seu comando foi invocado usando a API C funcionar **xlfCaller**. Para obter mais informações, consulte [xlfCaller](xlfcaller.md).
  
Iniciar na interface de usuário do Excel 2007 é muito diferente das versões anteriores. As funções da API C que permitem a adição e a exclusão de barras de menus personalizados, menus, submenus, itens de menu, barras de ferramentas personalizadas e botões de barra de ferramentas que ainda são suportadas na maioria dos casos. No entanto, eles podem não sempre disponibilize o item adicionado de forma que os usuários estão familiarizados com. Você deve verificar cuidadosamente se qualquer funcionalidade adicionada ainda pode ser acessado ou implementar uma personalização específicos da versão. Iniciando no Excel 2007 a interface do usuário é melhor personalizado usando um módulo de código gerenciado que pode então ser fortemente agrupado a seus comandos XLL.
  
## <a name="see-also"></a>Confira também

- [Criar XLLs](creating-xlls.md)
- [Chamar funções de XLL no Assistente de função ou nas caixas de diálogo Substituir](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
- [Gerenciador de Suplemento e Funções da Interface XLL](add-in-manager-and-xll-interface-functions.md)
- [Desenvolvimento de XLLs do Excel](developing-excel-xlls.md)



