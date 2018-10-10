---
title: 'Etapa 2: Inicializar a caixa de listagem Principal'
TOCTitle: 'Step 2: Initialize the Main List Box'
ms:assetid: 81e4dcfd-6ee0-b5f9-9ea3-026c38c26bf0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249562(v=office.15)
ms:contentKeyID: 48545967
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f2b6b4d79262796aa8e9090d673a439a550f042c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464388"
---
# <a name="step-2-initialize-the-main-list-box"></a>Etapa 2: Inicializar a caixa de listagem Principal


**Aplica-se a**: Access 2013 | Office 2013

## <a name="step-2-initialize-the-main-list-box"></a>Etapa 2: Inicializar a caixa de listagem Principal

**Para declarar os objetos Record e Recordset globais**

  - Insira o seguinte código em (General) (Declarations) para Form1:
    
    ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
    ```
    
    Este código declara as referências de objetos globais para os objetos **Record** e **Recordset** que serão usados posteriormente neste cenário.

**Para se conectar a um URL e preencher lstMain**

  - Insira o seguinte código no manipulador de eventos Form Load para Form1:
    
    ```vb 
     
    Private Sub Form_Load() 
        Set grec = New Record 
        Set grs = New Recordset 
        grec.Open "", "URL=https://servername/foldername/", , _ 
            adOpenIfExists Or adCreateCollection 
        Set grs = grec.GetChildren 
        While Not grs.EOF 
            lstMain.AddItem grs(0) 
            grs.MoveNext 
        Wend 
    End Sub 
    ```
    
    Este código instancia os objetos **Record** e **Recordset** globais. O **registro**, grec, é aberto com uma URL especificada como o **ActiveConnection**. Se o URL existir, estará aberto; se ainda não existir, será criado. Observe que você deveria substituir "https://servername/foldername/" por um URL válido a partir do seu ambiente. O **Recordset**, grs, é aberto nos filhos do **registro**, grec. Em seguida, lstMain é preenchido com os nomes dos arquivos dos recursos publicados no URL.

