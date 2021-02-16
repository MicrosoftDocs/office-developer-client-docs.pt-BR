---
title: Interfaces das janelas (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e6900ad7-c147-4816-93a9-5773170b115a
description: As interfaces Window e Windows são que objetos de API do OneNote 2013 que permitem que os usuários trabalhem com as janelas do OneNote. Esses objetos permitem que os usuários enumerem o conjunto das janelas do OneNote e modifiquem certas propriedades da janela.
ms.openlocfilehash: efc34312def588ecff54c63b3db84f8bf909352b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317029"
---
# <a name="window-interfaces-onenote"></a>Interfaces das janelas (OneNote)

As interfaces **Window** e **Windows** são objetos de API do OneNote 2013 que permitem que os usuários trabalhem com as janelas do OneNote. Esses objetos permitem que os usuários enumerem o conjunto das janelas do OneNote e modifiquem certas propriedades da janela. 
  
## <a name="onenote-window-views"></a>OneNote window views

A lista a seguir mostra os quatro modos de exibição que estão disponíveis para janelas do OneNote: 
  
- Modo de exibição normal, exibe a janela padrão do OneNote onde os painéis de navegação do bloco de anotações e da página estiverem visível.
    
- Total de exibição de página, exibe uma interface de usuário mínima (UI) onde os painéis de página e bloco de anotações não são exibidos.
    
- Anotação rápida, exibe uma pequena janela que permite aos usuários fazer anotações curtas. Anotações rápidas normalmente podem ser acessadas por meio do ícone do OneNote na área de notificação do Windows, mas você também pode acessá-los por meio do guia **modo de exibição** no OneNote. 
    
- Encaixar na área de trabalho, exibe uma janela do OneNote que você pode encaixar a qualquer lado da área de trabalho (semelhante à barra de tarefas). Esse modo de exibição reduz o tamanho da área de trabalho para ajustá-la a janela. Você pode encaixar apenas uma janela a qualquer momento e janela fica sempre visível sem bloquear a área de trabalho. 
    
A figura a seguir mostra como os itens modo de página inteira, encaixar na área de trabalho modo de exibição, e anotações rápidas são exibidos na área de trabalho.
  
**exibição do OneNote**

![Modos de exibição da janela OneNote](media/ON15Con_views.jpg "exibições de janela do OneNote")
  
## <a name="interfaces"></a>Interfaces

Esta seção lista as interfaces e membros que você pode usar para modificar as janelas do OneNote por programação.
  
### <a name="windows-interface"></a>Interface do Windows

A interface **Windows** também permite ao usuário acessar o conjunto de janelas abertas do OneNote. É uma propriedade do OneNote da classe **aplicativo** acessado por meio de **Application.Windows**. Isso retorna o conjunto enumerado de janelas do OneNote. 
  
**Propriedades**

|**Nome**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|**Contagem** <br/> |ULong  <br/> |Obtém o número dos objetos Window no **conjunto** do Windows.  <br/> |
|**CurrentWindow** <br/> |**Janela** <br/> |Obtém o objeto **janela** da janela ativa do OneNote.  <br/> |
|**Items** <br/> |**Janela** <br/> |Retorna o objeto **janela** que corresponde ao valor de índice passado. Essa propriedade não pode ser acessada diretamente. Para retornar um objeto **janela**, use **Windows [índice (uint)]**.  <br/> |
   
### <a name="window-interface"></a>Interface de janela

A interface **janela** também permite ao usuário acessar certas propriedades de cada janela. Cada janela do OneNote pode ser acessada por enumerar através da propriedade **Windows** da classe **aplicativo**. 
  
**Propriedades**

|**Nome**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|**Ativo** <br/> |bool  <br/> |Obtém ou define um valor que indica se a janela é a janela ativa do OneNote.  <br/> |
|**Application** <br/> |**Application** <br/> |Obtém o objeto **aplicativo** do OneNote que estão associados com a janela.  <br/> |
|**CurrentPageId** <br/> |string  <br/> |Obtém a ID de objeto da página do OneNote ativa da janela.  <br/> |
|**CurrentSectionId** <br/> |string  <br/> |Obtém a ID de objeto da seção do OneNote ativa da janela.  <br/> |
|**CurrentSectionGroupId** <br/> |string  <br/> |Obtém a ID de objeto da seção de grupo ativa da janela do OneNote.  <br/> |
|**CurrentNotebookId** <br/> |string  <br/> |Obtém a ID de objeto do bloco de anotações ativo na janela do OneNote.  <br/> |
|**DockedLocation** <br/> |**DockedLocation** <br/> |Obtém ou define a localização encaixada da janela do OneNote.  <br/> |
|**FullPageView** <br/> |bool  <br/> |Obtém ou define um valor que indica se a janela está no modo de exibição de página inteira (exibição mínima de interface do usuário).  <br/> |
|**SideNote** <br/> |bool  <br/> |Obtém ou define um valor que indica se a janela é uma janela de anotação rápida.  <br/> |
|**WindowHandle** <br/> |ULong  <br/> |É a ID de alça da janela do OneNote.  <br/> |
   
**Métodos**
  
Você pode usar os seguintes métodos das interfaces **janela** para acessar objetos específicos na janela do OneNote ou nas URLs especificadas. 
  
**NavigateTo**

|||
|:-----|:-----|
|**Descrição** <br/> |Leva até um objeto específico na janela do OneNote. Por exemplo, você pode navegar em seções, páginas elementos de estrutura das páginas.  <br/> |
|**Sintaxe** <br/> | `HRESULT NavigateTo(`           ` [in]BSTR bstrHierarchyObjectID, `           ` [in]BSTR bstrObjectID); ` <br/> |
|**Parâmetros** <br/> | _bstrHierarchyObjectID_: Hierarquia do OneNote ID do objeto que você quer navegar. A ID de objeto pode fazer referência a um bloco de anotações do OneNote, seção, grupo de seção ou página.  <br/>  _bstrObjectID_, a ID do OneNote de um objeto específico para navegar até em uma página do OneNote. Se o usuário não quiser navegar até um objeto específico em uma página, esse parâmetro será definido como nulo.  <br/> |
   
**NavigateToUrl**

|||
|:-----|:-----|
|**Descrição** <br/> |Se for passado um link do OneNote (onenote://), a janela do OneNote abre no local correspondente no OneNote. No entanto, se o link está um link externo, como https:// ou file://,uma caixa de diálogo de segurança aparecerá. Após a demissão, o OneNote tentará abrir o link e um erro HResult.hrObjectDoesNotExist será retornado.  <br/> |
|**Sintaxe** <br/> | `HRESULT NavigateToUrl (`           ` [in]BSTR bstrUrl); ` <br/> |
|**Parâmetros** <br/> | _bstrUrl_, a URL para navegar até.  <br/> |
   
**SetDockedLocation**

|||
|:-----|:-----|
|**Descrição** <br/> |Encaixa a janela na localização especificada por **dockLocation** e pelo monitor na **ptMonitor**.  <br/> |
|**Sintaxe** <br/> | `HRESULT SetDockedLocation`(           `[in] DockLocation dockLocation,`           `[in] POINT ptMonitor);` <br/> |
|**Parâmetros** <br/> | _dockLocation_ -indica o local encaixado de uma janela do OneNote 2013.  <br/>  _ptMonitor_ -(opcional) indica em coordenadas x,y em qual monitor a janela deve ser encaixada.  <br/> |
   
## <a name="example"></a>Exemplo

O seguinte código percorre o OneNote do windows para encontrar uma janela encaixada. Se não houver nenhuma janela encaixada, o exemplo encaixa a janela ativa. Se não houver nenhuma janela encaixada, o código criará uma nova janela encaixada.
  
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

- [Referência do desenvolvedor do OneNote](onenote-developer-reference.md)

