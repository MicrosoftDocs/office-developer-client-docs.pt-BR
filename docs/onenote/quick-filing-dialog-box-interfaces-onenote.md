---
title: Interfaces da caixa de diálogo de arquivamento rápido (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: d83e39f0-b259-4c33-8f3e-e03e94c2403d
description: Este tópico descreve as interfaces que você pode usar para personalizar programaticamente a caixa de diálogo de arquivamento rápido no OneNote 2013.
ms.openlocfilehash: dd6b28ae6cb2acb007bae26ea661facaf1f8d4be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425334"
---
# <a name="quick-filing-dialog-box-interfaces-onenote"></a>Interfaces da caixa de diálogo de arquivamento rápido (OneNote)

Este tópico descreve as interfaces que você pode usar para personalizar programaticamente a caixa de diálogo de arquivamento rápido no OneNote 2013.
  
## <a name="quick-filing-dialog-box"></a>Caixa de diálogo de arquivamento rápido

A caixa de diálogo de arquivamento rápido no OneNote 2013 é uma caixa de diálogo personalizável que permite que os usuários selecionem um local dentro da estrutura de hierarquia do OneNote. Locais selecionáveis incluem blocos de anotações, grupos de seções, seções, páginas e subpáginas. A caixa de diálogo é usada no aplicativo OneNote e por aplicativos externos por meio da API do OneNote 2013. A Figura 1 mostra a caixa de diálogo de arquivamento rápido em seu estado padrão.
  
**Figura 1. Caixa de diálogo de arquivamento rápido sem personalizações**

![Caixa de diálogo de arquivaMento rápido sem personalizações] (media/ON15Con_quick_filing_dialog.jpg "Caixa de diálogo de arquivaMento rápido sem personalizações")
  
Na caixa de diálogo, os usuários podem navegar na hierarquia de todos os blocos de anotações para procurar locais específicos ou pesquisar a estrutura de árvore do OneNote digitando na caixa de texto. Os aspectos da caixa de diálogo que podem ser personalizados incluem o título, a descrição, a lista de resultados recentes, o texto da caixa de seleção e o estado, a profundidade da árvore, os botões e os tipos de local selecionável.

Você pode acessar a funcionalidade de caixa de diálogo de arquivamento rápido através de duas interfaces do OneNote 2013. A interface **IQuickFilingDialog** permite que os usuários criem, configurem e executem a caixa de diálogo. A interface **IQuickFilingDialogCallback** é chamada depois que a caixa de diálogo é fechada. A caixa de diálogo é executada no processo do OneNote, portanto, um mecanismo é necessário para manter o thread da caixa de diálogo em execução e, em seguida, capturar a seleção do usuário e o estado da caixa de diálogo quando ele é fechado. 
  
## <a name="iquickfilingdialog-interface"></a>Interface IQuickFilingDialog
<a name="odc_IQuickFilingDialog"> </a>

Esta interface permite que o usuário personalize e execute a caixa de diálogo. O usuário pode criar uma instância de uma caixa de diálogo por meio da classe **Application** usando o método **Application. QuickFilingDialog** . O método retorna uma instância da caixa de diálogo. Após a definição das propriedades da caixa de diálogo, o método **IQuickFilingDialog. Run** é usado para executar a caixa de diálogo. Este método executa a caixa de diálogo em um novo thread. 
  
**Propriedades**

|**Nome**|**Type**|**Descrição**|
|:-----|:-----|:-----|
|**Title** <br/> |string  <br/> |Obtém ou define o texto do título que aparece na barra de título da janela da caixa de diálogo.  <br/> |
|**Descrição** <br/> |string  <br/> |Obtém ou define a descrição do texto para instruir o usuário sobre o que selecionar. Esse valor pode ser texto de várias linhas.  <br/> |
|**CheckboxText** <br/> |string  <br/> |Obtém ou define o texto que segue a caixa de seleção. Se esse valor for definido como uma cadeia de caracteres não vazia, uma caixa de seleção aparecerá na caixa de diálogo. Se o valor for uma sequência de caracteres vazia, nenhuma caixa de seleção será exibida.  <br/> |
|**CheckBoxState** <br/> |bool  <br/> |Obtém ou define o estado da caixa de seleção. Se value for definido como **false**, a caixa de seleção será desmarcada quando a caixa de diálogo for iniciada. Se o valor for definido como **true**, a caixa de seleção será marcada quando a caixa de diálogo for iniciada, desde que **CheckBoxText** seja uma cadeia de caracteres não vazia.  <br/> |
|**WindowHandle** <br/> |ULong  <br/> |Obtém a ID de identificador da janela da caixa de diálogo de arquivamento rápido.  <br/> |
|**TreeDepth** <br/> |**Hierarchyelement** <br/> |Obtém ou define a profundidade da árvore do OneNote que deve ser exibida na seção todos os blocos de anotações. Por padrão, a árvore é exibida até as seções. Essa propriedade não afeta o tipo de elementos que podem ser selecionados.  <br/> Se **TreeDepth** estiver definido como um elemento inferior na hierarquia do OneNote do que pode ser selecionado por qualquer um dos botões, a profundidade da árvore exibida será o elemento selecionável mais baixo possível. Ou seja, se a profundidade da árvore for definida para ser exibida para a página, mas o elemento selecionável mais baixo for uma seção, a árvore será exibida para baixo para as seções.  <br/> |
|**ParentWindowHandle** <br/> |ULong  <br/> |Obtém ou define a ID de identificador da janela pai da caixa de diálogo. Se essa propriedade for definida, a caixa de diálogo de arquivamento rápido será modal para a janela pai atribuída quando a caixa de diálogo for aberta. Ou seja, um usuário não poderá acessar a janela pai até que a caixa de diálogo de arquivamento rápido seja fechada.  <br/> |
|**Posição** <br/> |tagPOINT  <br/> |Obtém ou define a posição da janela em relação à tela. Por padrão, a caixa de diálogo aparece no meio da janela pai ou na área de trabalho.  <br/> |
|**SelectedItem** <br/> |string  <br/> |Obtém a ID de objeto do local do OneNote selecionado pelo usuário quando a caixa de diálogo é fechada. Se o usuário clicar no botão **Cancelar** , o objeto será definido como nulo.  <br/> |
|**PressedButton** <br/> |ULong  <br/> |Obtém qual botão foi clicado quando a caixa de diálogo foi fechada. Se o botão **Cancelar** foi clicado, essa propriedade retornará um valor de-1. Todos os outros botões são atribuídos valores inteiros de 0, incrementados por 1 para cada botão adicionado à caixa de diálogo. O valor inteiro do botão **OK** padrão é 0.  <br/> |
   
### <a name="methods"></a>Métodos

**SetRecentResults**

|||
|:-----|:-----|
|**Descrição** <br/> |Define o que a lista de resultados recentes será exibida na caixa de diálogo de arquivamento rápido e indica se inclui alguns locais especiais de arquivamento na lista. Os usuários podem selecionar uma lista de resultados recente da enumeração [RecentResultType](enumerations-onenote-developer-reference.md#odc_RecentResultType) . Os usuários também podem optar por adicionar as seguintes opções à lista: seção atual, página atual ou anotações não arquivadas. Se **RecentResultType. rrtNone** for selecionado, nenhuma lista de resultados recentes será mostrada.  <br/> |
|**Sintaxe** <br/> | `HRESULT SetRecentResults (`<br/>`[in]RecentResultType recentResults,`<br/>`[in]VARIANT_BOOL fShowCurrentSection,`<br/>`[in]VARIANT_BOOL fShowCurrentPage,`<br/>`[in]VARIANT_BOOL fShowUnfiledNotes);` <br/> |
|**Parâmetros** <br/> | _recentResults_ &ndash; Um objeto do tipo **RecentResultType** que indica qual lista de resultados recentes, se houver, deve ser exibida. Se **rrtNone** for selecionado, nenhuma lista de resultados recentes aparecerá na caixa de diálogo.<br/><br/>  _fShowCurrentSection_ &ndash; Um valor Boolean que indica se a seção atual deve ser incluída na lista de resultados recentes.<br/><br/>  _fShowCurrentPage_ &ndash; Um valor Boolean que indica se a página atual deve ser incluída na lista de resultados recentes.<br/><br/>  _fShowUnfiledNotes_ &ndash; Um valor Boolean que indica se a seção anotações não arquivadas deve ser incluída na lista de resultados recentes.  <br/> |
   
> [!NOTE]
> Se não for possível selecionar um local de arquivamento especial usando qualquer um dos botões da caixa de diálogo, ele não será exibido na lista. Se nenhum item selecionável na lista de resultados recentes for localizado, nenhuma lista de resultados recentes será exibida. 
  
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
|**Descrição** <br/> |Permite que os usuários adicionem e personalizem botões na caixa de diálogo. Os usuários podem especificar o texto nos botões e quais elementos da hierarquia do OneNote podem ser selecionados por cada botão.  <br/> |
|**Sintaxe** <br/> | `HRESULT AddButton (`<br/>`[in]BSTR bstrText,`<br/>`[in]HierarchyElement allowedElements,`<br/>`[in]HierarchyElement allowedReadOnlyElements,`<br/>`[in]VARIANT_BOOL fDefault);` <br/> |
|**Parâmetros** <br/> | _bstrText_ &ndash; Uma cadeia de caracteres que especifica o texto a ser exibido no botão. Para personalizar o botão **OK** padrão, passe um valor nulo como **bstrText**.  <br/><br/>_allowedElements_ &ndash; Um **hierarchyelement** que indica quais elementos de hierarquia do OneNote não somente leitura um usuário tem permissão para selecionar usando o botão. Para selecionar vários itens, o usuário deve passar o operador **or** para todos os valores equivalentes uint dos tipos **hierarchyelement** permitidos como hierarchyelement ****.<br/><br/>  _allowedReadOnlyElements_ &ndash; Um **hierarchyelement** que indica quais elementos de hierarquia somente leitura do OneNote um usuário tem permissão para selecionar usando o botão. Para selecionar vários itens, o usuário deve passar o operador **or** para todos os valores de equivalentes **uint** dos tipos **hierarchyelement** permitidos como hierarchyelement ****.<br/><br/>  _fDefault_ &ndash; Um valor booliano que especifica se esse botão deve ser o botão padrão. Se vários botões estiverem definidos como padrão, o último botão especificado se tornará o botão padrão.  <br/> |
   
O exemplo a seguir adiciona três botões à caixa de diálogo de arquivamento rápido. O primeiro, **todos**, pode ser selecionado por todos os elementos na árvore de hierarquia do OneNote. Os outros, **blocos de anotações** e **páginas**podem ser selecionados somente se seus elementos, blocos de anotações e páginas correspondentes estiverem selecionados.
  
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
|**Descrição** <br/> |Exibe a caixa de diálogo de arquivamento rápido a partir de um novo thread. Ele faz referência à interface **IQuickFilingDialogCallback** , cujo método **OnDialogClosed** será chamado depois que a caixa de diálogo for fechada.  <br/> |
|**Sintaxe** <br/> | `HRESULT Run (`<br/>`[in]IQuickFilingDialogCallback piCallback);` <br/> |
|**Parâmetros** <br/> | _piCallback_ &ndash; Uma referência à interface **IQuickFilingDialogCallback** que será instanciada quando a caixa de diálogo for fechada.  <br/> |
   
O exemplo a seguir usa o método **Run** para exibir a caixa de diálogo de arquivamento rápido a partir de um novo thread. 
  
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
|**Descrição** <br/> |Indica se a árvore hierárquica deve ser expandida ou recolhida.  <br/> |
|**Sintaxe** <br/> | `HRESULT TreeCollapsedState(`<br/>`[in] TreeCollapsedStateType tcs);` <br/> |
|**Parâmetros** <br/> | _TCS_ -especifica se a árvore está expandida ou recolhida.  <br/> |
   
**NotebookFilterOut**

|||
|:-----|:-----|
|**Descrição** <br/> |Filtra a lista de blocos de anotações mostrados por tipo.  <br/> |
|**Sintaxe** <br/> | `HRESULT NotebookFilterOut(`<br/>`[in] NotebookFilterOutType nfo);` <br/> |
|**Parâmetros** <br/> | _NFO_ -especifica o conjunto de blocos de anotações que devem ser filtrados da lista  <br/> |
   
**ShowCreateNewNotebook**

|||
|:-----|:-----|
|**Descrição** <br/> |Exibe a opção Criar novo bloco de anotações na caixa de diálogo.  <br/> |
|**Sintaxe** <br/> | `HRESULT ShowCreateNewNotebook ();` <br/> |
|**Parâmetros** <br/> |Nenhum  <br/> |
   
**AddInitialEditor**

|||
|:-----|:-----|
|**Descrição** <br/> |Adiciona um usuário como um editor inicial a um bloco de anotações na caixa de diálogo de arquivamento rápido.  <br/> |
|**Sintaxe** <br/> | `HRESULT AddInitialEditor (BSTR initialEditor);` <br/> |
|**Parâmetros** <br/> | _initialEditor_ -o endereço de email do usuário que você deseja adicionar como um editor ao bloco de anotações. Quando o bloco de anotações é criado por meio da caixa de diálogo de arquivamento rápido, ele é automaticamente compartilhado com todos os editores iniciais.  <br/> |
   
**ClearInitialEditors**

|||
|:-----|:-----|
|**Descrição** <br/> |Remove todos os editores iniciais da caixa de diálogo de arquivamento rápido.  <br/> |
|**Sintaxe** <br/> | `HRESULT ClearInitialEditors ();` <br/> |
|**Parâmetros** <br/> |Nenhum  <br/> |
   
**ShowSharingHyperlink**

|||
|:-----|:-----|
|**Descrição** <br/> |Exibe o hiperlink do tópico da ajuda de compartilhamento na caixa de diálogo de arquivamento rápido.  <br/> |
|**Sintaxe** <br/> | `HRESULT ShowSharingHyperlink();` <br/> |
|**Parâmetros** <br/> |Nenhum  <br/> |
   
## <a name="iquickfilingdialogcallback-interface"></a>Interface IQuickFilingDialogCallback
<a name="odc_IQuickFilingDialog"> </a>

Essa interface permite que o usuário acesse as propriedades da caixa de diálogo após o fechamento da caixa de diálogo. Depois que a caixa de diálogo é fechada, o OneNote 2013 chama o método **IQuickFilingDialogCallback. OnDialogClose** nesta interface. 
  
Uma classe que herda esta interface deve ser definida.
  
### <a name="methods"></a>Métodos

A seção a seguir descreve os métodos associados às interfaces detalhadas anteriormente.
  
**OnDialogClosed**

|||
|:-----|:-----|
|**Descrição** <br/> |Permite que os usuários adicionem funcionalidade para capturar e usar a seleção de usuário na caixa de diálogo. Este método é chamado depois que a caixa de diálogo de arquivamento rápido é fechada. Este método é uma função que as interfaces do **IQuickFilingDialogCallback** precisam definir.  <br/> |
|**Sintaxe** <br/> | `HRESULT OnDialogClosed (`<br/>`[in]IQuickFilingDialog dialog);` <br/> |
|**Parâmetros** <br/> | _caixa de diálogo_ &ndash; O objeto **IQuickFilingDialog** que chamou o método **OnDialogClose** .  <br/> |
   
O exemplo a seguir é uma interface **IQuickFilingDialogCallback** de exemplo. O método **OnDialogClose** imprime a seleção do usuário da caixa de diálogo de arquivamento rápido no console. 
  
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

## <a name="example"></a>Exemplo
<a name="odc_IQuickFilingDialog"> </a>

O exemplo de código a seguir abre uma caixa de diálogo de arquivamento rápido que tem um título personalizado, uma descrição, uma lista de resultados recentes, a profundidade da árvore, a caixa de seleção e os botões. O item selecionado do usuário, o botão pressionado e o estado da caixa de seleção serão exibidos em uma janela do console quando a caixa de diálogo for fechada. Para ver o botão de página habilitado, o usuário terá que procurar por uma página e selecioná-la, pois a profundidade da árvore é definida para as seções. A caixa de diálogo não é um filho de nenhuma janela.
  
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

- [Referência do desenvolvedor do OneNote](onenote-developer-reference.md)

