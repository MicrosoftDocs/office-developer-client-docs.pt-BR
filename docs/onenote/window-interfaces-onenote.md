---
title: Interfaces de janela (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e6900ad7-c147-4816-93a9-5773170b115a
description: As interfaces de janela e janelas são que objetos de API do OneNote 2013 que permite que os usuários trabalhem com janelas do OneNote. Esses objetos permitem aos usuários enumerar toda o conjunto de janelas do OneNote e modificar determinadas propriedades de janela.
ms.openlocfilehash: 83a3742419a4c8faf11c22c4766744d675151c1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765794"
---
# <a name="window-interfaces-onenote"></a>Interfaces de janela (OneNote)

As interfaces de **janela** e **janelas** são que objetos de API do OneNote 2013 que permite que os usuários trabalhem com janelas do OneNote. Esses objetos permitem aos usuários enumerar toda o conjunto de janelas do OneNote e modificar determinadas propriedades de janela. 
  
## <a name="onenote-window-views"></a>OneNote window views

A lista a seguir mostra os modos de exibição de quatro que você pode usar para janelas do OneNote: 
  
- Modo de exibição normal — exibe a janela do OneNote padrão no qual os painéis de navegação do bloco de anotações e página estão visíveis.
    
- Total de modo de exibição de página — exibe uma mínima interface do usuário (UI) exibir na qual os painéis de bloco de anotações e a página não são exibidos.
    
- Anotação rápida — exibe uma pequena janela que permite que os usuários façam anotações curtas. Notas Rápidas geralmente podem ser acessadas por meio do ícone do OneNote na área de notificação do Windows, mas você também pode acessá-los por meio da guia **Exibir** no OneNote. 
    
- Encaixa à área de trabalho — exibe uma janela do OneNote que é possível encaixar para qualquer lado da área de trabalho (semelhante à barra de tarefas). Este modo de exibição reduz o tamanho da área de trabalho para se ajustar na janela. É possível encaixar apenas uma janela a qualquer momento, e a janela é sempre visível sem bloqueio da área de trabalho. 
    
A figura a seguir mostra qual a exibição de página inteira, encaixar na exibição da área de trabalho, e notas rápidas se parecem na área de trabalho.
  
**Modos de exibição do OneNote**

![Exibições de janela do OneNote] (media/ON15Con_views.jpg "Exibições de janela do OneNote")
  
## <a name="interfaces"></a>Interfaces

Esta seção lista as interfaces e os membros que você pode usar para modificar as janelas do OneNote programaticamente.
  
### <a name="windows-interface"></a>Interface do Windows

A interface do **Windows** permite que o usuário acesse o conjunto de janelas do OneNote abertas. É uma propriedade da classe do OneNote **aplicativo** , acessada por meio de **Application**. Isso retorna o conjunto enumerado de janelas do OneNote. 
  
**Properties**

|**Nome**|**Type**|**Descrição**|
|:-----|:-----|:-----|
|**Count** <br/> |ULong  <br/> |Obtém o número de objetos **Window** no conjunto de **Windows** .  <br/> |
|**CurrentWindow** <br/> |**Window** <br/> |Obtém o objeto de **janela** da janela ativa do OneNote.  <br/> |
|**Items** <br/> |**Window** <br/> |Retorna o objeto de **janela** que corresponde ao valor de índice passado. Essa propriedade não pode ser acessada diretamente. Para retornar um objeto **Window** , use **Windows [índice (uint)]**.  <br/> |
   
### <a name="window-interface"></a>Interface da janela

A interface de **janela** permite que o usuário acesse determinadas propriedades de cada janela. Cada janela OneNote pode ser acessada pela enumeração por meio da propriedade **Windows** da classe **Application** . 
  
**Properties**

|**Nome**|**Type**|**Descrição**|
|:-----|:-----|:-----|
|**Active** <br/> |bool  <br/> |Obtém ou define um valor que indica se a janela é a janela ativa do OneNote.  <br/> |
|**Application** <br/> |**Application** <br/> |Obtém o objeto de **aplicativo** do OneNote que está associado à janela.  <br/> |
|**CurrentPageId** <br/> |string  <br/> |Obtém a ID de objeto do OneNote page ativo da janela.  <br/> |
|**CurrentSectionId** <br/> |string  <br/> |Obtém a ID de objeto da seção OneNote ativa da janela.  <br/> |
|**CurrentSectionGroupId** <br/> |string  <br/> |Obtém a ID de objeto do grupo de seção do OneNote ativo da janela.  <br/> |
|**CurrentNotebookId** <br/> |string  <br/> |Obtém a ID de objeto do bloco de anotações do OneNote ativo da janela.  <br/> |
|**DockedLocation** <br/> |**DockedLocation** <br/> |Obtém ou define o local ancorado da janela do OneNote.  <br/> |
|**FullPageView** <br/> |bool  <br/> |Obtém ou define um valor que indica se a janela está no modo de exibição de página inteira (exibição de UI mínima).  <br/> |
|**Anotação rápida** <br/> |bool  <br/> |Obtém ou define um valor que indica se a janela é uma janela de anotação rápida.  <br/> |
|**WindowHandle** <br/> |ULong  <br/> |Obtém a identificação da alça da janela do OneNote.  <br/> |
   
**Métodos**
  
Você pode usar os seguintes métodos da interface da **janela** para navegar para os objetos especificados na janela do OneNote ou URLs especificadas. 
  
**Navegarpara**

|||
|:-----|:-----|
|**Descrição** <br/> |Navega para o objeto especificado na janela do OneNote. Por exemplo, você pode navegar para os elementos de estrutura de tópicos dentro de páginas, páginas e seções.  <br/> |
|**Sintaxe** <br/> | `HRESULT NavigateTo(`           ` [in]BSTR bstrHierarchyObjectID, `           ` [in]BSTR bstrObjectID); ` <br/> |
|**Parameters** <br/> | _bstrHierarchyObjectID_— a hierarquia do OneNote ID do objeto que você deseja navegar. A ID de objeto pode fazer referência a um notebook OneNote, seção, grupo de seção ou página.  <br/>  _bstrObjectID_— o ID do OneNote do objeto específico para navegar até dentro de uma página do OneNote. Se não quiser que o usuário navegar para um objeto específico em uma página, esse parâmetro for definido como null.  <br/> |
   
**NavigateToUrl**

|||
|:-----|:-----|
|**Descrição** <br/> |Se passar um link do OneNote (onenote: / /), abre a janela do OneNote para o local correspondente no OneNote. No entanto, se o link é um link externo, como http:// ou file://, será exibida uma caixa de diálogo segurança. Após a demissão, OneNote tenta abrir o link e é retornado um erro de HResult.hrObjectDoesNotExist.  <br/> |
|**Sintaxe** <br/> | `HRESULT NavigateToUrl (`           ` [in]BSTR bstrUrl); ` <br/> |
|**Parameters** <br/> | _bstrUrl_— o URL para navegar até.  <br/> |
   
**SetDockedLocation**

|||
|:-----|:-----|
|**Descrição** <br/> |Encaixa a janela para o local especificado pelo **dockLocation** e o monitor em **ptMonitor**.  <br/> |
|**Sintaxe** <br/> | `HRESULT SetDockedLocation`(           `[in] DockLocation dockLocation,`           `[in] POINT ptMonitor);` <br/> |
|**Parameters** <br/> | _dockLocation_ - indica a localização ancorada de uma janela do OneNote 2013.  <br/>  _ptMonitor_ - indica (opcional) em x, coordenadas y que monitorar a janela deve ser encaixado.  <br/> |
   
## <a name="example"></a>Example

O código a seguir itera-se as janelas do OneNote para encontrar uma janela encaixada. Se nenhuma janela encaixada existir, o exemplo encaixa a janela ativa. Se nenhuma janela ativa existir, o código cria uma nova janela encaixada.
  
```cs
using System;
using System.Diagnostics;
using Microsoft.Office.Interop.OneNote;
namespace SampleWND
{
    class DockOneNoteWindow
    {
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = new Microsoft.Office.Interop.OneNote.Application();
            // Search through all OneNote windows for a docked window and activate it.
            bool foundDockedWND = false;
            for (int i = 0; i < app.Windows.Count; i++)
            {
                if (app.Windows[(uint) i].DockedLocation != DockLocation.dlNone)
                {
                    foundDockedWND = true;
                    app.Windows[(uint) i].Active = true;
                }
            }
            
            // If no docked window exists, dock the active window.
            if (!foundDockedWND && (app.Windows.Count > 0))
                app.Windows.CurrentWindow.DockedLocation = DockLocation.dlDefault;
            // If no active window exists, create a new docked window.
            if (app.Windows.Count < 1)
            {
                Process oneProc = new Process();
                oneProc.StartInfo.FileName = "onenote.exe";
                oneProc.StartInfo.Arguments = "/docked";
                oneProc.Start();
            }
        }
    }
}

```

## <a name="see-also"></a>Confira também

- [Referência para desenvolvedores do OneNote](onenote-developer-reference.md)

