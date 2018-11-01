---
title: Objeto Recordset (ADO)
TOCTitle: Recordset Object (ADO)
ms:assetid: 0f963bf8-f066-dc8a-b754-f427de712df1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248865(v=office.15)
ms:contentKeyID: 48543267
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 26172a73f0967ef299b79e0bae30088eec0f77c9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872582"
---
# <a name="recordset-object-ado"></a>Objeto Recordset (ADO)

**Aplica-se a**: Access 2013, o Office 2013

Representa o conjunto completo de registros de uma tabela base ou os resultados de um comando executado. Sempre que for adequado, o objeto **Recordset** fará referência somente a um único registro do conjunto como o registro atual.

## <a name="remarks"></a>Comentários

Use os objetos **Recordset** para manipular os dados de um provedor. Quando você usa o ADO, manipula os dados de forma quase completa usando os objetos **Recordset**. Todos os objetos **Recordset** são compostos de registros (linhas) e campos (colunas). Dependendo da funcionalidade suportada pelo provedor, alguns métodos ou propriedades **Recordset** podem não estar disponíveis.

ADODB.Recordset é o ProgID que deve ser usado para criar um objeto **Recordset**. Os aplicativos existentes que fazem referência ao ADOR.Recordset ProgID desatualizado continuarão funcionando sem recompilação, mas o novo desenvolvimento deverá fazer referência ao ADODB.Recordset.

Existem quatro tipos de cursores diferentes definidos no ADO:

  - **Cursor dinâmico**  possibilita a exibição de adições, alterações e exclusões de outros usuários; permite todos os tipos de movimento por meio do **Recordset** que não conta com indicadores e aceita indicadores se o provedor oferecer suporte.

  - **Cursor controlado por conjuntos de chaves**  se comporta como um cursor dinâmico, exceto pelo fato de impedir que você veja os registros adicionados por outros usuários e não permitir o acesso aos registros excluídos por outros usuários. As alterações de dados feitas por outros usuários permanecerão visíveis. Oferece suporte para indicadores e, por esse motivo, possibilita todos os tipos de movimento por meio do **Recordset**.

  - **Cursor estático**  fornece uma cópia estática do conjunto de registros usado para localizar dados ou gerar relatórios; sempre aceita indicadores e, por esse motivo, permite todos os tipos de movimento por meio do **Recordset**. Não serão visíveis adições, alterações ou exclusões dos outros usuários. Este será o único tipo de cursor permitido quando você abrir o objeto **Recordset** do cliente.

  - **Cursor apenas de avanço**  permite somente o avanço do **Recordset**. Não serão visíveis adições, alterações ou exclusões dos outros usuários. Isso melhora o desempenho em situações nas quais você precisar fazer somente uma única passagem em um **Recordset**.

Defina a propriedade [CursorType](cursortype-property-ado.md) antes de abrir o **Recordset** para escolher o tipo de cursor ou passar um argumento *CursorType* com o método [Open](open-method-ado-recordset.md) . Alguns provedores não suportam todos os tipos de cursores. Verifique a documentação do provedor. Se você não especificar um tipo de cursor, o ADO abrirá o cursor apenas de avanço por padrão.

Se a propriedade [CursorLocation](cursorlocation-property-ado.md) está definida como **adUseClient** para abrir um **Recordset**, a propriedade **UnderlyingValue** nos objetos [Field](field-object-ado.md) não estará disponível no objeto **Recordset** retornado. Quando usada com alguns provedores (como o Microsoft ODBC Provider for OLE DB em conjunto com o Microsoft SQL Server), permite criar objetos **Recordset** de forma independente de um objeto [Connection](connection-object-ado.md) definido anteriormente por meio da passagem de uma sequência de conexão com o método **Open**. O ADO ainda criará um objeto [Connection](connection-object-ado.md), mas não atribuirá esse objeto a uma variável de objeto. No entanto, se você está abrindo vários objetos **Recordset** na mesma conexão, deverá criar e abrir, de forma explícita, um objeto **Connection**; isso atribuirá o objeto **Connection** a uma variável de objeto. Se você não usar essa variável de objeto ao abrir os objetos **Recordset**, o ADO criará um novo objeto **Connection** para cada novo **Recordset**, ainda que você passe a mesma sequência de conexão.

Crie quantos objetos **Recordset** forem necessários.

Quando você abrir um **Recordset**, o registro atual será posicionado no primeiro registro (se houver) e as propriedades [BOF](bof-eof-properties-ado.md) e [EOF](bof-eof-properties-ado.md) serão definidas como **False**. Se não houver registros, as definições das propriedades **BOF** e **EOF** serão **True**.

Use os métodos [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), **MoveLast**, **MoveNext** e **MovePrevious**; o método [Move](move-method-ado.md); e as propriedades [AbsolutePosition](absoluteposition-property-ado.md), [AbsolutePage](absolutepage-property-ado.md) e [Filter](filter-property-ado.md) para reposicionar o registro atual, supondo que o provedor ofereça suporte para a funcionalidade relevante. Os objetos **Recordset** somente de encaminhamento oferecem suporte apenas para o método [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md). Quando você usar os métodos **Move** para visitar cada registro (ou enumerar o **Recordset**), poderá usar as propriedades **BOF** e **EOF** para determinar se você se moveu além do inicio ou do final do **Recordset**.

Os objetos **Recordset** oferecem suporte a dois tipos de atualização: imediata e em lotes. Na atualização imediata, todas as alterações dos dados são gravadas imediatamente na fonte de dados base assim que você chamar o método [Update](update-method-ado.md). Também é possível passar matrizes de valores como parâmetros com os métodos [AddNew](addnew-method-ado.md) e **Update** e atualizar simultaneamente vários campos de um registro.

Se um provedor oferecer suporte para a atualização em lotes, você terá as alterações do cache do provedor para mais de um registro e depois irá transmiti-las em uma única chamada para o banco de dados com o método [UpdateBatch](updatebatch-method-ado.md). Isso se aplica a alterações feitas com os métodos **AddNew**, **Update** e [Delete](delete-method-ado-recordset.md). Depois de chamar o método **UpdateBatch**, use a propriedade [Status](status-property-ado-recordset.md) para procurar quaisquer conflitos de dados e resolvê-los.

> [!NOTE]
> [!OBSERVAçãO] Para executar uma consulta sem usar o objeto [Command](command-object-ado.md), passe uma sequência de consulta para o método **Open** de um objeto **Recordset**. No entanto, um objeto **Command** será necessário quando você desejar insistirno texto de comando e reexecutá-lo ou usar os parâmetros de consulta.

A propriedade [Mode](mode-property-ado.md) governa as permissões de acesso.

A coleção **Fields** é o membro padrão do objeto **Recordset**. Como resultado, as duas instruções de código a seguir são equivalentes.

```vb
    Debug.Print objRs.Fields.Item(0)  ' Both statements print 
    Debug.Print objRs(0)              '  the Value of Item(0).
```
