---
title: Cenário de Publicação de Internet
TOCTitle: Internet publishing scenario
ms:assetid: 25a3fa8b-86ec-9e72-5e62-bf0d849479b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249024(v=office.15)
ms:contentKeyID: 48543790
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0f28b14f3eaf6792a74ef0967d698d5a3914955a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291269"
---
# <a name="internet-publishing-scenario"></a>Cenário de Publicação de Internet

**Aplica-se ao:** Access 2013, Office 2013

Este exemplo de código demonstra como usar o ADO com o Provedor DB Microsoft OLE para Publicação na Internet. Neste cenário, você criará um aplicativo do Visual Basic que usa os objetos **Recordset**, **Record** e **Stream** para exibir o conteúdo dos recursos publicados com o Internet Publishing Provider.

As seguintes etapas são necessárias para criar este cenário: 

1. Configurar o projeto do Visual Basic.
2. Inicializar a caixa de listagem principal.
3. Preencha a caixa de listagem campos.
4. Preencha a caixa de texto detalhes.

## <a name="step-1-set-up-the-visual-basic-project"></a>Etapa 1: configurar o projeto do Visual Basic

Neste cenário, considera-se que você tem o Microsoft Visual Basic 6.0 ou posterior, ADO 2.5 ou posterior e o Microsoft OLE DB Provider for Internet Publishing instalado no seu sistema.

### <a name="create-an-ado-project"></a>Criar um projeto do ADO

1.  No Microsoft Visual Basic, crie um novo projeto EXE padrão.

2.  No menu **Projeto**, clique em **Referências**.

3.  Selecione **biblioteca do Microsoft ActiveX Data objects 2,5**e clique em **OK**.

### <a name="insert-controls-on-the-main-form"></a>Inserir controles no formulário principal

1.  Adicione um controle ListBox em Form1. Defina sua propriedade **Name** como **lstMain**.

2.  Adicione outro controle ListBox em Form1. Defina sua propriedade **Name** como **lstDetails**.

3.  Adicione um controle TextBox em Form1. Defina sua propriedade **Name** como **txtDetails**.

## <a name="step-2-initialize-the-main-list-box"></a>Etapa 2: inicializar a caixa de listagem principal

### <a name="declare-global-record-and-recordset-objects"></a>Declarar objetos Record e Recordset globais

- Insira o seguinte código em (General) (Declarations) para Form1:
    
   ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
   ```
    
   Este código declara as referências de objetos globais para os objetos **Record** e **Recordset** que serão usados posteriormente neste cenário.

### <a name="connect-to-a-url-and-populate-lstmain"></a>Conectar-se a uma URL e preencher lstMain

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
    
   Este código instancia os objetos **Record** e **Recordset** globais. O **registro** `grec` é aberto com uma URL especificada como **ActiveConnection**. Se o URL existir, estará aberto; se ainda não existir, será criado. 
   
   Observe que você deve substituir `https://servername/foldername/` por uma URL válida do seu ambiente. 
   
   O **Recordset** `grs` é aberto nos filhos do **registro** `grec`. O lstMain é preenchido com os nomes de arquivo dos recursos publicados na URL.

## <a name="step-3-populate-the-fields-list-box"></a>Etapa 3: preencher a caixa de listagem campos

- Insira o seguinte código no manipulador de eventos Click de lstMain:

   ```vb 
    
    Private Sub lstMain_Click() 
        Dim rec As Record 
        Dim rs As Recordset 
        Set rec = New Record 
        Set rs = New Recordset 
        grs.MoveFirst 
        grs.Move lstMain.ListIndex 
        lstDetails.Clear 
        rec.Open grs 
        Select Case rec.RecordType 
            Case adCollectionRecord: 
                Set rs = rec.GetChildren 
                While Not rs.EOF 
                    lstDetails.AddItem rs(0) 
                    rs.MoveNext 
                Wend 
            Case adSimpleRecord: 
                recFields rec, lstDetails, txtDetails 
                
            Case adStructDoc: 
        End Select 
        
    End Sub 
   ```

   Este código declara e instancia os objetos `rec` **Record** e **Recordset** local e, `rs`respectivamente.

   A linha correspondente ao recurso selecionado em lstMain é feita a linha atual de `grs`. A caixa de listagem **detalhes** é desmarcada e `rec` aberta com a linha atual `grs` da como a fonte.

   Se o recurso for um registro de coleção (conforme especificado **** por RecordType), o **Recordset** `rs` local será aberto nos filhos de `rec`. lstDetails é preenchido com os valores das linhas de `rs`.

   Se o recurso for um registro simples, `recFields` o será chamado. Para obter mais informações `recFields`sobre o, consulte a próxima etapa.

   Nenhum código será implementado se o recurso for um documento estruturado.

## <a name="step-4-populate-the-details-text-box"></a>Etapa 4: preencher a caixa de texto detalhes

- Crie uma nova subrotina nomeada `recFields` e insira o seguinte código:

   ```vb 
    
    Sub recFields(r As Record, l As ListBox, t As TextBox) 
        Dim f As Field 
        Dim s As Stream 
        Set s = New Stream 
        Dim str As String 
        
        For Each f In r.Fields 
            l.AddItem f.Name & ": " & f.Value 
        Next 
        t.Text = "" 
        If r!RESOURCE_CONTENTCLASS = "text/plain" Then 
            s.Open r, adModeRead, adOpenStreamFromRecord 
            str = s.ReadText(1) 
            s.Position = 0 
            If Asc(Mid(str, 1, 1)) = 63 Then '//63 = "?" 
                s.Charset = "ascii" 
                s.Type = adTypeText 
            End If 
            t.Text = s.ReadText(adReadAll) 
        End If 
    End Sub 
   ```

   Este código preenche lstDetails com os campos e valores do registro simples passados para `recFields`. Se o registro for um arquivo de texto, um texto **Stream** será aberto a partir do registro de recurso. O código determina se o conjunto de caracteres é ASCII e copia o **** conteúdo do fluxo `txtDetails`para.

