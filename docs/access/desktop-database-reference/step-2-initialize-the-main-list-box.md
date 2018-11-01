---
title: 'Etapa 2: Inicializar a caixa de listagem Principal'
TOCTitle: 'Step 2: Initialize the Main List Box'
ms:assetid: 81e4dcfd-6ee0-b5f9-9ea3-026c38c26bf0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249562(v=office.15)
ms:contentKeyID: 48545967
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3505c2726da3f2f2f01d179c97cde5a1d7b635ba
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869894"
---
# <a name="step-2-initialize-the-main-list-box"></a>Etapa 2: Inicializar a caixa de listagem Principal


**Aplica-se a**: Access 2013, o Office 2013

## <a name="step-2-initialize-the-main-list-box"></a>Etapa 2: Inicializar a caixa de listagem principal

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

