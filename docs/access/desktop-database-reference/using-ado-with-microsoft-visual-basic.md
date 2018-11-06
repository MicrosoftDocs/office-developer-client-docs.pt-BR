---
title: Usando o ADO com o Microsoft Visual Basic
TOCTitle: Using ADO with Microsoft Visual Basic
ms:assetid: 5e0fb2ec-42aa-e181-386f-099607ac7400
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249338(v=office.15)
ms:contentKeyID: 48545130
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a405189f3130a24c98112f0b0d9f31c7bfa4c217
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997746"
---
# <a name="using-ado-with-microsoft-visual-basic"></a>Usando o ADO com o Microsoft Visual Basic

**Aplica-se a**: Access 2013, o Office 2013

A configuração de um projeto ADO e a criação de um código ADO é semelhante quando você usa o Visual Basic ou o Visual Basic for Applications. Este tópico aborda o uso do ADO com o Visual Basic e o Visual Basic for Applications e indica as diferenças.

## <a name="referencing-the-ado-library"></a>Referenciando a biblioteca ADO

A biblioteca ADO deve ser referenciada pelo seu projeto.

### <a name="to-reference-ado-from-microsoft-visual-basic"></a>Para fazer referência ao ADO a partir do Microsoft Visual Basic

1. No Visual Basic, no menu **Projeto**, selecione **Referências...**.

2. Selecione **Biblioteca Microsoft ActiveX Data Objects x.x** na lista. Verifique se pelo menos as bibliotecas a seguir também estão selecionadas:
   
   - Visual Basic for Applications
   - Procedimentos e objetos em tempo de execução do Visual Basic
   - Procedimentos e objetos do Visual Basic
   - Automação OLE

3. Clique em **OK**.

Você pode usar o ADO facilmente com o Visual Basic for Applications, por meio do Microsoft Access, por exemplo.

### <a name="to-reference-ado-from-microsoft-access"></a>Para fazer referência ao ADO a partir do Microsoft Access

1. No Microsoft Access, selecione ou crie um módulo a partir da guia **Módulos** na janela **Banco de dados**.

2. No menu **Ferramentas**, selecione **Referências...**.

3. Selecione **Biblioteca Microsoft ActiveX Data Objects x.x** na lista. Verifique se pelo menos as bibliotecas a seguir também estão selecionadas:
    
   - Visual Basic for Applications
   - Biblioteca de objetos do Microsoft Access 11.0 (ou posterior)

4. Clique em **OK**.

## <a name="creating-ado-objects-in-visual-basic"></a>Criando objetos ADO no Visual Basic

Para criar uma variável de automação e uma instância de um objeto para essa variável, você pode usar dois métodos: **Dim** ou **CreateObject**.

### <a name="dim"></a>Dim

Use a palavra-chave **New** com **Dim** para declarar e instanciar objetos ADO em uma única etapa:

```vb 
 
Dim conn As New ADODB.Connection 
```

Opcionalmente, a declaração de instrução **Dim** e a instanciação de objeto também pode ter duas etapas:

```vb 
 
Dim conn As ADODB.Connection 
Set conn = New ADODB.Connection 
```

> [!NOTE]
> Ele não é necessário usar explicitamente ADODB progid com a instrução **Dim** , supondo que você referenciou corretamente a biblioteca ADO em seu projeto. Entretanto, sua utilização garante a ausência de conflitos de nomeação com outras bibliotecas.
> 
> Por exemplo, se você incluir referências a ADO e a DAO no mesmo projeto, inclua um qualificador para especificar qual modelo de objeto será usado ao instanciar objetos **Recordset**, como no código a seguir:  
> 
> `Dim adoRS As ADODB.Recordset`  
>   
> `Dim daoRS As DAO.Recordset`

### <a name="createobject"></a>CreateObject

Com o método **CreateObject**, a declaração e a instanciação de objeto deverá ter duas etapas separadas:

```vb 
 
Dim conn1 
Set conn1 = CreateObject("ADODB.Connection") As Object 
```

Os objetos instanciados com **CreateObject** são acoplados posteriormente, ou seja, eles não são do tipo de alta segurança, e a conclusão da linha de comando estará desabilitada. Entretanto, com ele, você não precisará fazer referência à biblioteca ADO a partir de seu projeto e poderá instanciar versões específicas de objetos. Por exemplo:

```vb 
 
Set conn1 = CreateObject("ADODB.Connection.2.0") As Object 
```

Você também pode fazer isso desenvolvendo uma referência específica à biblioteca de tipos ADO versão 2.0 e criando o objeto.

A instanciação de objetos com o método **CreateObject** geralmente é mais lenta do que o uso da instrução **Dim**.

## <a name="handling-events"></a>Manipular eventos

Para lidar com eventos do ADO no Microsoft Visual Basic, você deve declarar uma variável de nível de módulo usando a palavra-chave **WithEvents** . É possível declarar a variável somente como parte de um módulo de classe e é necessário declará-la no nível do módulo. Para uma abordagem mais completa sobre manipulação de eventos do ADO, consulte [Capítulo 7: eventos do ADO manipulação](chapter-7-handling-ado-events.md).

## <a name="visual-basic-examples"></a>Exemplos do Visual Basic

Vários exemplos de Visual Basic são incluídos com a documentação do ADO. Para obter mais informações, consulte [exemplos de código ADO no Microsoft Visual Basic](ado-code-examples-in-microsoft-visual-basic.md).

