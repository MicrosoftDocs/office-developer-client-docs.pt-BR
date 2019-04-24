---
title: O objeto Field (referência do banco de dados de área de trabalho do Access)
TOCTitle: The Field object
ms:assetid: 55531e04-d74f-6394-df64-1660e5d572ca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249284(v=office.15)
ms:contentKeyID: 48544926
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2cbd5752399e5a14f08b7eb944e3a028ba53f561
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314018"
---
# <a name="field-object"></a>Objeto Field

**Aplica-se ao:** Access 2013, Office 2013

Cada objeto **Field** normalmente corresponde a uma coluna em uma tabela de banco de dados. No entanto, um **Field** também pode representar um ponteiro para outro **Recordset**, chamado de capítulo. Exceções, como colunas de capítulo, serão abordadas posteriormente neste guia.

Use a propriedade **Value** de objetos **Field** para definir ou retornar dados do registro atual. Dependendo da funcionalidade apresentada pelo provedor, algumas coleções, métodos ou propriedades de um objeto **Field** talvez não estejam disponíveis.

Com as coleções, os métodos e as propriedades de um objeto **Field**, você pode fazer o seguinte:

- Retornar o nome de um campo usando a propriedade **Name**.

- Exibir ou alterar os dados do campo usando a propriedade **Value**. **Value** é a propriedade padrão do objeto **Field**.

- Retorne as características básicas de um campo usando as propriedades **Type**, **Precision** e **NumericScale**.

- Retorne um tamanho declarada de um campo usando a propriedade **DefinedSize**.

- Retorne o tamanho real dos dados em determinado campo usando a propriedade **ActualSize**.

- Determine a quais tipos de funcionalidade há suporte em determinado campo, usando a propriedade **Attributes** e a coleção **Properties**.

- Manipule os valores dos campos que contêm dados binários longos e de caracteres longos, usando os métodos **AppendChunk** e **GetChunk**.

- Resolva discrepâncias nos valores dos campos durante as atualizações em lotes, usando as propriedades **OriginalValue** e **UnderlyingValue**, se o provedor oferecer suporte a essas atualizações.

## <a name="describing-a-field"></a>Descrevendo um campo

Os tópicos a seguir abordarão as propriedades do objeto [Field](field-object-ado.md) que representam informações descritivas do próprio objeto **Field**, isto é, metadados sobre o campo. É possível usar essas informações para determinar vários aspectos sobre o esquema do **Recordset**. Essas propriedades incluem **Type**, **DefinedSize** e **ActualSize**, bem como **Name**, **NumericScale** e **Precision**.

## <a name="discovering-the-data-type"></a>Descobrindo o tipo de dados

A propriedade **Type** indica o tipo de dados do campo. As constantes enumeradas de tipo de dados que são suportadas pelo ADO estão descritas em [DataTypeEnum](datatypeenum.md) na *referência do programador do ADO*.

É possível obter mais informações sobre os tipos numéricos de ponto flutuante, como **adNumeric**. A propriedade **NumericScale** indica quantos dígitos à direita do ponto decimal serão usados para representar valores do **Field**. A propriedade **Precision** especifica o número máximo de dígitos usados para representar valores do **Field**.

## <a name="determining-field-size"></a>Determinando o tamanho do campo

Use a propriedade **DefinedSize** para determinar a capacidade de dados de um objeto **Field**.

Use a propriedade **ActualSize** para retornar o valor real de um objeto **Field**. Em todos os campos, a propriedade **ActualSize** é somente leitura. Se o ADO não puder determinar o valor do objeto **Field**, a propriedade **ActualSize** retornará **adUnknown**.

As propriedades **DefinedSize** e **ActualSize** tem finalidades diferentes. Por exemplo, considere um objeto **Field** com o tipo declarado **adVarChar** e o valor 50 da propriedade **DefinedSize**, contendo um único caractere. O valor da propriedade **ActualSize** retornado por ele é o tamanho em bytes do caractere único.

## <a name="determining-field-contents"></a>Determinando o conteúdo do campo

O identificador da coluna da fonte de dados é representado pela propriedade **Name** do **Field**. A propriedade **Value** do objeto **Field** retorna ou define o conteúdo real dos dados do campo. Essa é a propriedade padrão.

Para alterar os dados em um campo, defina a propriedade **Value** como um novo valor do tipo correto. O tipo de seu cursor deve oferecer suporte a atualizações para que o conteúdo de um campo seja alterado. A validação do banco de dados não é feita aqui no modo em lotes; portanto, você precisará verificar os erros quando chamar **UpdateBatch** nesse caso. Alguns provedores também oferecem suporte às propriedades **UnderlyingValue** e **OriginalValue** do objeto **Field** do ADO para ajudá-lo a solucionar conflitos quando você tentar realizar atualizações em lotes. Para obter detalhes sobre como solucionar esses conflitos, consulte o [Capítulo 4: Editando dados](chapter-4-editing-data.md).

> [!NOTE]
> [!OBSERVAçãO] Não é possível definir os valores do campo **Recordset** durante o acréscimo de novos objetos **Field** a um **Recordset**. Em vez disso, é possível acrescentar novos objetos **Field** a um **Recordset** fechado. Em seguida, o **Recordset** deverá ser aberto, e só então valores poderão ser atribuídos a esses objetos **Field**.

## <a name="getting-more-field-information"></a>Obtendo mais informações de campos

Os objetos do ADO têm dois tipos de propriedades: internas e dinâmicas. Até esse ponto, foram abordadas somente as propriedades internas do objeto **Field**.

Propriedades internas são aquelas implementadas no ADO e disponibilizadas imediatamente para qualquer objeto novo, usando a sintaxe. Elas não são exibidas como objetos **Property** na coleção **Properties** de um objeto.

As propriedades dinâmicas são definidas pelo provedor de dados subjacentes e aparecem na coleção **Properties** referente ao objeto ADO adequado. Por exemplo, uma propriedade específica do provedor pode indicar se um objeto **Recordset** oferece suporte a transações ou à atualização. Essas propriedades adicionais serão exibidas como objetos **Property** na coleção **Properties** do objeto **Recordset**. Propriedades dinâmicas podem ser referenciadas somente através da coleção, usando a sintaxe MyObject. Properties (0) ou MyObject. Properties ("Name").

Não é possível excluir nenhum tipo de propriedade.

Um objeto **Property** dinâmico tem quatro propriedades internas próprias:

- A propriedade **Name** é uma sequência de caracteres que identifica a propriedade.

- A propriedade **Type** é um inteiro que especifica o tipo de dados da propriedade.

- A propriedade **Value** é uma variante que contém a definição da propriedade. **Value** é a propriedade padrão de um objeto **Property**.

- A propriedade **Attributes** é um valor **Long** que indica características da propriedade específica do provedor.

A coleção **Properties** do objeto **Field** contém metadados adicionais sobre o campo. O conteúdo dessa coleção varia de acordo com o provedor. O exemplo de código a seguir examina a coleção **Properties** do **Recordset** de exemplo apresentado no início deste capítulo. Primeiro, ele observa o conteúdo da coleção. Esse código usa o [OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), de modo que a coleção **Properties** contenha informações relevantes a esse provedor.

```vb 
 
'BeginFieldProps 
 Dim objProp As ADODB.Property 
 
 For intLoop = 0 To (objFields.Count - 1) 
 Debug.Print objFields.Item(intLoop).Name 
 
 For Each objProp In objFields(intLoop).Properties 
 Debug.Print vbTab & objProp.Name & " = " & objProp.Value 
 Next objProp 
 Next intLoop 
'EndFieldProps 
```

## <a name="dealing-with-binary-data"></a>Lidando com dados binários

Use o método [AppendChunk](appendchunk-method-ado.md) em um objeto **Field** para preenchê-lo com dados binários ou de caracteres longos. Em situações em que a memória do sistema é limitada, você pode usar o método **AppendChunk** para manipular valores longos em partes, e não em sua totalidade.

Se o bit **adFldLong** na propriedade **Attributes** de um objeto **Field** for definido como **True**, você poderá usar o método **AppendChunk** nesse campo.

A primeira chamada de **AppendChunk** em um objeto **Field** grava dados no campo, substituindo os dados existentes. As chamadas subsequentes de **AppendChunk** fazem adições aos dados existentes. Se você estiver acrescentando dados a um campo e, depois, definir ou ler o valor de outro campo no registro atual, o ADO presumirá que o acréscimo de dados ao primeiro campo foi concluído. Se você chamar o método **AppendChunk** no primeiro campo novamente, o ADO interpretará a chamada como uma nova operação de **AppendChunk** e substituirá os dados existentes. O acesso a campos em outros objetos **Recordset** que não sejam clones do primeiro objeto **Recordset** não interromperá as operações de **AppendChunk**.

Use o método **GetChunk** em um objeto **Field** para recuperar parte ou todos os seus dados binários ou de caracteres longos. Em situações em que a memória do sistema é limitada, você pode usar o método **GetChunk** para manipular valores longos em partes, e não em sua totalidade.

Os dados retornados por **GetChunk** são atribuídos a *variable*. Se *Size* for maior que os dados restantes, o método **GetChunk** retornará somente esses dados sem preencher *variable* com espaços vazios. Se o campo estiver vazio, o método **GetChunk** retornará um valor nulo.

Cada chamada subsequente de **GetChunk** recupera dados a partir do ponto em que a chamada anterior de **GetChunk** foi interrompida. Contudo, se você estiver recuperando dados de um campo e, em seguida, definir ou ler o valor de outro campo do registro atual, o ADO presumirá que foi concluída a recuperação de dados no primeiro campo. Se você chamar o método **GetChunk** no primeiro campo novamente, o ADO interpretará a chamada como uma nova operação de **GetChunk** e iniciará a leitura desde o início dos dados. O acesso a campos em outros objetos **Recordset** que não sejam clones do primeiro objeto **Recordset** não interromperá as operações de **GetChunk**.

Se o bit **adFldLong** na propriedade **Attributes** de um objeto **Field** for definido como **True**, será possível utilizar o método **GetChunk** nesse campo.

Se não houver um registro atual quando você usar o método **GetChunk** ou **AppendChunk** em um objeto **Field**, ocorrerá o erro 3021 (sem registro atual).

Para obter um exemplo de como usar esses métodos para manipular dados binários, consulte os exemplos do método [AppendChunk](appendchunk-method-ado.md) e do [método GetChunk](getchunk-method-ado.md) na *referência do programador do ADO*.

