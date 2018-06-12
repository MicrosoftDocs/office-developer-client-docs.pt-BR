---
title: Interfaces de caixa de diálogo de arquivamento rápidos (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: d83e39f0-b259-4c33-8f3e-e03e94c2403d
description: Este tópico descreve as interfaces que você pode usar para personalizar programaticamente a caixa de diálogo arquivamento rápido no OneNote 2013.
ms.openlocfilehash: d2647ed4d7b9f4487c033260eba8df1e4281c6ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765784"
---
# <a name="quick-filing-dialog-box-interfaces-onenote"></a>Interfaces de caixa de diálogo de arquivamento rápidos (OneNote)

Este tópico descreve as interfaces que você pode usar para personalizar programaticamente a caixa de diálogo arquivamento rápido no OneNote 2013.
  
## <a name="quick-filing-dialog-box"></a>Caixa de diálogo arquivamento rápida

A caixa de diálogo arquivamento rápido no OneNote 2013 é uma caixa de diálogo personalizável que permite que os usuários selecionem um local dentro da estrutura de hierarquia do OneNote. Selecionáveis locais incluem os blocos de anotações, grupos de seção, seções, páginas e subpáginas. A caixa de diálogo é usada dentro do aplicativo do OneNote e por aplicativos externos por meio da API do OneNote 2013. A Figura 1 mostra a caixa de diálogo Preenchimento rápido em seu estado padrão.
  
**Figura 1. Caixa de diálogo arquivamento rápida sem personalizações**

![Caixa de diálogo Preenchimento rápido sem personalizações] (media/ON15Con_quick_filing_dialog.jpg "Caixa de diálogo Preenchimento rápido sem personalizações")
  
Dentro da caixa de diálogo, os usuários podem navegar na hierarquia de todos os blocos de anotações para procurar locais específicos ou pesquise a estrutura de árvore do OneNote digitando na caixa de texto. Aspectos da caixa de diálogo que podem ser personalizados incluem o título, descrição, recentes lista de resultados, caixa de seleção de texto e estado, profundidade de árvore, botões e tipos de localização selecionável.

Você pode acessar a funcionalidade de caixa de diálogo Preenchimento rápido por meio de duas interfaces do OneNote 2013. A interface **IQuickFilingDialog** permite que os usuários criar uma instância, configurar e executar a caixa de diálogo. A interface **IQuickFilingDialogCallback** é chamada depois que a caixa de diálogo é fechada. A caixa de diálogo é executada no processo do OneNote, portanto um mecanismo é necessário para manter um segmento da caixa de diálogo em execução e, em seguida, para capturar a seleção do usuário e o estado da caixa de diálogo quando ele for fechado. 
  
## <a name="iquickfilingdialog-interface"></a>Interface de IQuickFilingDialog
<a name="odc_IQuickFilingDialog"> </a>

Essa interface permite ao usuário personalizar e executar a caixa de diálogo. O usuário pode instanciar uma caixa de diálogo por meio da classe de **aplicativo** usando o método **Application.QuickFilingDialog** . O método retorna uma instância da caixa de diálogo. Depois que as propriedades da caixa de diálogo estiverem definidas, o método **IQuickFilingDialog.Run** é usado para a caixa de diálogo Executar. Esse método executa a caixa de diálogo em um novo segmento. 
  
**Properties**

|**Nome**|**Type**|**Descrição**|
|:-----|:-----|:-----|
|**Title** <br/> |string  <br/> |Obtém ou define o texto do título aparece na barra de título da janela de caixa de diálogo.  <br/> |
|**Descrição** <br/> |string  <br/> |Obtém ou define a descrição de texto para instruir o usuário sobre o que selecionar. Esse valor pode ser texto com várias linhas.  <br/> |
|**CheckboxText** <br/> |string  <br/> |Obtém ou define o texto que segue a caixa de seleção. Se esse valor é definido como uma cadeia de caracteres não-vazias, uma caixa de seleção é exibida na caixa de diálogo. Se o valor for uma sequência vazia, nenhuma caixa de seleção é exibida.  <br/> |
|**CheckboxState** <br/> |bool  <br/> |Obtém ou define o estado da caixa de seleção. Se o valor for definido como **false**, a caixa de seleção está desmarcada, quando a caixa de diálogo é iniciada. Se o valor for definido como **true**, a caixa de seleção é selecionada quando a caixa de diálogo é iniciada desde que o **CheckboxText** é uma cadeia de caracteres não vazias.  <br/> |
|**WindowHandle** <br/> |ULong  <br/> |Obtém a identificação da alça da janela de caixa de diálogo Preenchimento rápido.  <br/> |
|**TreeDepth** <br/> |**HierarchyElement** <br/> |Obtém ou define a profundidade, a árvore do OneNote deve ser exibida na seção de todos os blocos de anotações. Por padrão, a árvore é exibida até as seções. Essa propriedade não afeta a que tipo de elementos que pode ser selecionado.  <br/> Se **TreeDepth** estiver definida como um elemento inferior na hierarquia do OneNote, que pode ser selecionado por qualquer um dos botões, a profundidade de árvore exibida será o menor elemento selecionável possível. Ou seja, se profundidade da árvore está definida para exibir para baixo até páginas, mas o elemento selecionável mais baixa é uma seção, a árvore é exibida para baixo até seções.  <br/> |
|**ParentWindowHandle** <br/> |ULong  <br/> |Obtém ou define a ID do identificador da janela pai da caixa de diálogo. Se essa propriedade estiver definida, a caixa de diálogo Preenchimento rápido será restrita para a janela pai atribuído quando a caixa de diálogo será aberta. Ou seja, um usuário não será capaz de acessar a janela pai até que a caixa de diálogo Preenchimento rápido seja fechada.  <br/> |
|**Position** <br/> |tagPOINT  <br/> |Obtém ou define a posição da janela em relação à tela. Por padrão, a caixa de diálogo aparece no meio da janela pai ou a área de trabalho.  <br/> |
|**SelectedItem** <br/> |string  <br/> |Obtém a ID de objeto do OneNote local selecionado pelo usuário quando a caixa de diálogo é fechada. Se o usuário clicar no botão **Cancelar** , o objeto é definido como null.  <br/> |
|**PressedButton** <br/> |ULong  <br/> |Obtém a qual botão foi clicado quando a caixa de diálogo foi fechada. Se o botão **Cancelar** foi clicado, essa propriedade retorna um valor de -1. Todos os outros botões recebem valores inteiros de 0, incrementada em 1 para cada botão adicionado à caixa de diálogo. O valor de inteiro do botão de **Okey** padrão é 0.  <br/> |
   
### <a name="methods"></a>Métodos

**SetRecentResults**

|||
|:-----|:-----|
|**Descrição** <br/> |Define a lista de resultados que recentes será exibida na caixa de diálogo Preenchimento rápido e indica se é necessário incluir alguns locais de arquivamento especiais na lista. Os usuários podem selecionar a lista de resultados recentes provenientes da enumeração [RecentResultType](enumerations-onenote-developer-reference.md#odc_RecentResultType) . Os usuários também podem optar por adicionar as seguintes opções na lista: seção atual, a página atual ou anotações não arquivadas. Se **RecentResultType.rrtNone** for selecionado, nenhuma lista de resultados recentes é mostrada.  <br/> |
|**Sintaxe** <br/> | `HRESULT SetRecentResults (`<br/>`[in]RecentResultType recentResults,`<br/>`[in]VARIANT_BOOL fShowCurrentSection,`<br/>`[in]VARIANT_BOOL fShowCurrentPage,`<br/>`[in]VARIANT_BOOL fShowUnfiledNotes);` <br/> |
|**Parameters** <br/> | _recentResults_ &ndash; Um objeto do tipo **RecentResultType** que indica qual recentes lista de resultados, se houver, deve aparecer. Se **rrtNone** for selecionado, nenhuma lista de resultados recentes aparece na caixa de diálogo.<br/><br/>  _fShowCurrentSection_ &ndash; Um valor Boolean que indica se a seção atual deve ser incluída na lista de resultados recentes.<br/><br/>  _fShowCurrentPage_ &ndash; Um valor Boolean que indica se a página atual deve ser incluída na lista de resultados recentes.<br/><br/>  _fShowUnfiledNotes_ &ndash; Um valor Boolean que indica se a seção anotações não arquivadas deve ser incluída na lista de resultados recentes.  <br/> |
   
> [!NOTE]
> Se um local de arquivamento especiais não pode ser selecionado usando qualquer um dos botões na caixa de diálogo, ele não será mostrado na lista. Se nenhum item selecionável na lista de resultados recentes for localizado, nenhuma recentes lista de resultados será exibida. 
  
O exemplo a seguir usa o método **SetRecentResults** para exibir a seção atual, a página atual e a seção anotações não arquivadas na lista de resultados recentes. 
  
```cs
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            // RECENT RESULTS
            qfDialog.SetRecentResults(RecentResultType.rrtFiling,
                /*Current Section*/ true,
                /*Current Page*/ true,
                /*Unfiled Notes*/ true);
            ...
        }

```

**AddButton**

|||
|:-----|:-----|
|**Descrição** <br/> |Permite aos usuários adicionar e personalizar os botões na caixa de diálogo. Os usuários podem especificar o texto sobre os botões e quais elementos da hierarquia do OneNote podem ser selecionados por cada botão.  <br/> |
|**Sintaxe** <br/> | `HRESULT AddButton (`<br/>`[in]BSTR bstrText,`<br/>`[in]HierarchyElement allowedElements,`<br/>`[in]HierarchyElement allowedReadOnlyElements,`<br/>`[in]VARIANT_BOOL fDefault);` <br/> |
|**Parameters** <br/> | _bstrText_ &ndash; Uma cadeia de caracteres que especifica o texto a ser exibido no botão. Para personalizar o botão de **Okey** padrão, passe um valor nulo como **bstrText**.  <br/><br/>_allowedElements_ &ndash; **HierarchyElement** que indica quais elementos de hierarquia do OneNote não somente leitura que um usuário tem permissão para selecionar usando o botão. Para selecionar vários itens, o usuário deve passar no operador **ou** para todos os valores equivalentes de uint dos tipos de **HierarchyElement** permitidos como um **HierarchyElement**.<br/><br/>  _allowedReadOnlyElements_ &ndash; **HierarchyElement** que indica quais elementos de hierarquia de somente leitura do OneNote que um usuário tem permissão para selecionar usando o botão. Para selecionar vários itens, o usuário deve passar no operador **ou** para todos os valores de equivalentes **uint** dos tipos de **HierarchyElement** permitidos como um **HierarchyElement**.<br/><br/>  _fDefault_ &ndash; Um valor Boolean que especifica se este botão deve ser o botão padrão. Se vários botões estiverem definidos como padrão, o último botão especificado torna-se o botão padrão.  <br/> |
   
O exemplo a seguir adiciona três botões à caixa de diálogo arquivamento rápido. Uma primeira, **todos**, pode ser selecionada por todos os elementos na árvore de hierarquia do OneNote. Os outros, **blocos de anotações** e **páginas**, podem ser selecionados somente se seus elementos correspondentes, blocos de anotações e páginas, estão selecionados.
  
```cs
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            
            // BUTTONS
            HierarchyElement heAll = (HierarchyElement) 
                ((uint)HierarchyElement.heNotebooks | 
                (uint)HierarchyElement.heSectionGroups | 
                (uint)HierarchyElement.heSections |  
                (uint)HierarchyElement.hePages);
            
            qfDialog.AddButton("All", heAll, heAll, true);
            qfDialog.AddButton("Notebooks", HierarchyElement.heNotebooks, 
                HierarchyElement.heNotebooks, false);
            qfDialog.AddButton("Pages", HierarchyElement.hePages, 
                HierarchyElement.hePages, false);
            ... 
        }

```

**Run**

|||
|:-----|:-----|
|**Descrição** <br/> |Exibe a caixa de diálogo Preenchimento rápido de um novo segmento. Ele utiliza uma referência para a interface **IQuickFilingDialogCallback** , cujo método **OnDialogClosed** será chamado depois que a caixa de diálogo é fechada.  <br/> |
|**Sintaxe** <br/> | `HRESULT Run (`<br/>`[in]IQuickFilingDialogCallback piCallback);` <br/> |
|**Parameters** <br/> | _piCallback_ &ndash; Uma referência para a interface de **IQuickFilingDialogCallback** que será instanciada depois que a caixa de diálogo é fechada.  <br/> |
   
O exemplo a seguir usa o método **Run** para exibir a caixa de diálogo Preenchimento rápido de um novo segmento. 
  
```cs
    class OpenQuickFilingDialog
    {
            ... 
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            // Display Quick Filing UI
            qfDialog.Run(new Callback());
            ... 
        }
    }

```

**TreeCollapsedState**

|||
|:-----|:-----|
|**Descrição** <br/> |Indica se a árvore de hierarquia deve ser expandido ou recolhido.  <br/> |
|**Sintaxe** <br/> | `HRESULT TreeCollapsedState(`<br/>`[in] TreeCollapsedStateType tcs);` <br/> |
|**Parameters** <br/> | _tcs_ - Especifica se a árvore é expandida ou recolhida.  <br/> |
   
**NotebookFilterOut**

|||
|:-----|:-----|
|**Descrição** <br/> |Filtra a lista de blocos de anotações mostrado por tipo.  <br/> |
|**Sintaxe** <br/> | `HRESULT NotebookFilterOut(`<br/>`[in] NotebookFilterOutType nfo);` <br/> |
|**Parameters** <br/> | _nfo_ - Especifica o conjunto de blocos de anotações que devem ser filtrados para fora da lista  <br/> |
   
**ShowCreateNewNotebook**

|||
|:-----|:-----|
|**Descrição** <br/> |Exibe a opção de criar novo bloco de anotações na caixa de diálogo.  <br/> |
|**Sintaxe** <br/> | `HRESULT ShowCreateNewNotebook ();` <br/> |
|**Parameters** <br/> |None  <br/> |
   
**AddInitialEditor**

|||
|:-----|:-----|
|**Descrição** <br/> |Adiciona um usuário como um editor inicial a um bloco de anotações na caixa de diálogo arquivamento rápido.  <br/> |
|**Sintaxe** <br/> | `HRESULT AddInitialEditor (BSTR initialEditor);` <br/> |
|**Parameters** <br/> | _initialEditor_ - o endereço de email do usuário que deseja adicionar como um editor como o bloco de anotações. Quando o bloco de anotações é criado por meio da caixa de diálogo Preenchimento rápido, ele é automaticamente compartilhado com todos os editores inicial.  <br/> |
   
**ClearInitialEditors**

|||
|:-----|:-----|
|**Descrição** <br/> |Remove todos os editores iniciais da caixa de diálogo arquivamento rápido.  <br/> |
|**Sintaxe** <br/> | `HRESULT ClearInitialEditors ();` <br/> |
|**Parameters** <br/> |None  <br/> |
   
**ShowSharingHyperlink**

|||
|:-----|:-----|
|**Descrição** <br/> |Exibe o hiperlink de tópico da Ajuda do compartilhamento na caixa de diálogo arquivamento rápido.  <br/> |
|**Sintaxe** <br/> | `HRESULT ShowSharingHyperlink();` <br/> |
|**Parameters** <br/> |None  <br/> |
   
## <a name="iquickfilingdialogcallback-interface"></a>Interface de IQuickFilingDialogCallback
<a name="odc_IQuickFilingDialog"> </a>

Essa interface permite ao usuário acessar as propriedades de caixa de diálogo depois que a caixa de diálogo é fechada. Depois que a caixa de diálogo é fechada, o OneNote 2013 chama o método **IQuickFilingDialogCallback.OnDialogClose** nesta interface. 
  
Uma classe que herda essa interface deve ser definido.
  
### <a name="methods"></a>Métodos

A seção a seguir descreve os métodos associados com as interfaces detalhadas anteriormente.
  
**OnDialogClosed**

|||
|:-----|:-----|
|**Descrição** <br/> |Permite que os usuários adicionam funcionalidade para capturar e usar a seleção de usuário da caixa de diálogo. Este método é chamado depois que a caixa de diálogo Preenchimento rápido é fechada. Esse método é uma função que **IQuickFilingDialogCallback** interfaces precisará definir.  <br/> |
|**Sintaxe** <br/> | `HRESULT OnDialogClosed (`<br/>`[in]IQuickFilingDialog dialog);` <br/> |
|**Parameters** <br/> | _diálogo_ &ndash; o objeto de **IQuickFilingDialog** que chamou o método **OnDialogClose** .  <br/> |
   
O exemplo a seguir é uma interface de **IQuickFilingDialogCallback** de amostra. O método **OnDialogClose** imprime a seleção do usuário da caixa de diálogo arquivamento rápido no console. 
  
```cs
    class Callback : IQuickFilingDialogCallback
    {
        public Callback(){}
        public void OnDialogClosed(IQuickFilingDialog qfDialog)
        {
            Console.WriteLine(qfDialog.SelectedItem);
            Console.WriteLine(qfDialog.PressedButton);
            Console.WriteLine(qfDialog.CheckboxState);
        }
    }

```

## <a name="example"></a>Example
<a name="odc_IQuickFilingDialog"> </a>

O exemplo de código a seguir abre uma caixa de diálogo Preenchimento rápido que tem um título personalizado, descrição, a lista de resultados recentes, profundidade de árvore, caixa de seleção e botões. O usuário selecionou o item, pressionado o botão e o estado da caixa de seleção será exibido em uma janela do console quando a caixa de diálogo é fechada. Para ver o botão página habilitado, o usuário terá que pesquisar uma página e selecioná-lo, porque a profundidade de árvore está definida para baixo às seções. A caixa de diálogo não é um filho de qualquer janela.
  
```cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading;
using Microsoft.Office.Interop.OneNote;
namespace SampleQFD
{
    class OpenQuickFilingDialog
    {
        private static EventWaitHandle wh = new AutoResetEvent(false);
        private static IQuickFilingDialog qfDialog;
        private static String strTitle = "Sample Title";
        private static String strDescription = "Sample Description";
        private static String strCheckboxText = "Sample Checkbox";
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            // Instantiate Quick Filing UI
            qfDialog = app.QuickFiling();
            #region//SET API PARAMETERS
            // TITLE
            qfDialog.Title = strTitle;
            // DESCRIPTION
            qfDialog.Description = strDescription;
            // RECENT RESULTS
            qfDialog.SetRecentResults(RecentResultType.rrtFiling,
                /*Current Section*/ true,
                /*Current Page*/ true,
                /*Unfiled Notes*/ true);
            // TREE DEPTH
            qfDialog.TreeDepth = HierarchyElement.heSections;
            // CHECKBOX
            qfDialog.CheckboxText = strCheckboxText;
            qfDialog.CheckboxState = false;
            // BUTTONS
            HierarchyElement heAll = (HierarchyElement) 
                ((uint)HierarchyElement.heNotebooks | 
                (uint)HierarchyElement.heSectionGroups | 
                (uint)HierarchyElement.heSections |  
                (uint)HierarchyElement.hePages);
            
            qfDialog.AddButton("All", heAll, heAll, true);
            qfDialog.AddButton("Notebooks", HierarchyElement.heNotebooks, 
                HierarchyElement.heNotebooks, false);
            qfDialog.AddButton("Pages", HierarchyElement.hePages, 
                HierarchyElement.hePages, false);
            // PARENTWINDOW
            #endregion
            // Display Quick Filing UI
            qfDialog.Run(new Callback());
            // Clean up and Wait so console window does not close
            qfDialog = null;
            wh.WaitOne();
        }
    }
    class Callback : IQuickFilingDialogCallback
    {
        public Callback(){}
        public void OnDialogClosed(IQuickFilingDialog qfDialog)
        {
            Console.WriteLine(qfDialog.SelectedItem);
            Console.WriteLine(qfDialog.PressedButton);
            Console.WriteLine(qfDialog.CheckboxState);
        }
    }
}

```

## <a name="see-also"></a>Confira também

- [Referência para desenvolvedores do OneNote](onenote-developer-reference.md)

