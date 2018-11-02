---
title: Método Append (ADO)
TOCTitle: Append method (ADO)
ms:assetid: cca133af-2b95-877d-0488-0d99631623f2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250014(v=office.15)
ms:contentKeyID: 48547742
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 03a953b34932a5090ab40abbc7613e3518506070
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925650"
---
# <a name="append-method-ado"></a>Método Append (ADO)


**Aplica-se a**: Access 2013, o Office 2013



Acrescenta um objeto a uma coleção. Se a coleção for [Fields](fields-collection-ado.md), um novo objeto [Field](field-object-ado.md) poderá ser criado antes de ser acrescentado à coleção.

## <a name="syntax"></a>Sintaxe

*coleção*. Acrescentar *objeto*

*campos*. Acrescentar o *nome*, *tipo*, *DefinedSize*, *Attrib*, *FieldValue*

## <a name="parameters"></a>Parâmetros

  - *collection*

  - Um objeto de coleção.

  - *fields*

  - A coleção **Fields**.

  - *object*

  - Uma variável de objeto que representa o objeto a ser acrescentado.

  - *Name*

  - Um valor **String** que contém o nome do novo objeto **Field** e deve ser diferente de qualquer outro nome de objeto em *fields*.

  - *Type*

  - Um valor [DataTypeEnum](datatypeenum.md), cujo valor padrão é **adEmpty**, que especifica o tipo de dados do novo campo. Os tipos de dados a seguir não são aceitos pelo ADO e não devem ser usados no acréscimo de novos campos a um **Recordset**: **adIDispatch**, **adIUnknown**, **adVariant**.

  - *DefinedSize*

  - Opcional. Um valor **Long** que representa o tamanho definido, em caracteres ou bytes, do novo campo. O valor padrão deste parâmetro é derivado de *Type*. Campos com DefinedSize maior que 255 bytes e tratados como colunas de comprimento variável. (O *DefinedSize* padrão não é especificado.)

  - *Attrib*

  - Opcional. Um valor [FieldAttributeEnum](fieldattributeenum.md), cujo valor padrão é **adFldDefault**, que especifica os atributos do novo campo. Se esse valor não for especificado, o campo conterá os atributos derivados de *Type*.

  - *FieldValue*

  - Opcional. Um **Variant** que representa o valor do novo campo. Se nenhum valor for especificado, o campo será acrescentado com um valor nulo.

## <a name="remarks"></a>Comentários

**Coleção Parameters**

Defina a propriedade [Type](type-property-ado.md) de um objeto [Parameter](parameter-object-ado.md) antes de acrescentá-la à coleção **Parameters**. Se selecionar um tipo de dados de comprimento variável, defina também a propriedade [Size](size-property-ado.md) para um valor maior que zero.

Você conseguirá diminuir as chamadas para o provedor ao descrever sozinho os parâmetros, melhorando consequentemente o desempenho com a utilização de procedimentos armazenados ou consultas com parâmetros. Entretanto, é necessário que você conheça as propriedades dos parâmetros associados ao procedimento armazenado ou à consulta com parâmetros a ser chamada.

Use o método [CreateParameter](createparameter-method-ado.md) para criar objetos **Parameter** com as configurações de propriedade adequadas e use o método **Append** para adicioná-los à coleção [Parameters](parameters-collection-ado.md). Isso permitirá definir e retornar valores de parâmetro sem que seja necessário chamar o provedor para as informações de parâmetro. Se estiver criando em um provedor que não fornece informações de parâmetro, use esse método para preencher manualmente a coleção **Parameters** e usar parâmetros.

**Coleção Fields**

O parâmetro *FieldValue* é válido apenas ao adicionar um objeto **Field** de um objeto [Record](record-object-ado.md) , não para um objeto **Recordset** . Com um objeto **Record**, você poderá acrescentar campos e fornecer valores simultaneamente. Com um objeto **Recordset**, você deverá criar campos enquanto **Recordset** estiver fechado e, em seguida, abrir o **Recordset** e atribuir valores aos campos.


> [!NOTE]
> Para novos objetos **Field** que foram acrescentados à coleção **Fields** de um objeto **Record**, a propriedade [Value](value-property-ado.md) deverá ser definida antes que qualquer outra propriedade **Field** seja especificada. Primeiro, um valor específico para a propriedade **Value** deve ser atribuído e o método [Update](update-method-ado.md) deve ser chamado na coleção **Fields**. Assim, outras propriedades, como [Type](type-property-ado.md) ou [Attributes](attributes-property-ado.md), poderão ser acessadas.


Os objetos **Field** dos seguintes tipos de dados (**DataTypeEnum**) não podem ser acrescentados à coleção **Fields**, caso contrário, causarão erro: **adArray**, **adChapter**, **adEmpty**, **adPropVariant** e **adUserDefined**. Os seguintes tipos de dados também não são aceitos pelo ADO: **adIDispatch**, **adIUnknown** e **adIVariant**. Para esses tipos, não ocorrerá erro quando eles forem acrescentados, mas o uso poderá produzir resultados inesperados, incluindo vazamentos de memória.

**Objeto Recordset**

Se você não definir a propriedade [CursorLocation](cursorlocation-property-ado.md) antes de chamar o método **Append**, **CursorLocation** será definido automaticamente como **adUseClient** (valor [CursorLocationEnum](cursorlocationenum.md)) quando o método [Open](recordset-object-ado.md) do objeto [Recordset](open-method-ado-recordset.md) for chamado.

Um erro em tempo de execução ocorrerá se o método **Append** for chamado na coleção **Fields** de um **Recordset** aberto, ou em um **Recordset** no qual foi definida a propriedade [ActiveConnection](activeconnection-property-ado.md). Você somente poderá acrescentar campos a um **Recordset** que não esteja aberto e que ainda não tenha sido conectado a uma fonte de dados, o que geralmente é o caso quando um objeto **Recordset** é fabricado com o método [CreateRecordset](createrecordset-method-rds.md) ou atribuído a uma variável de objeto.

**Objeto Record**

Um erro em tempo de execução não ocorrerá se o método **Append** for chamado na coleção **Fields** de um **Record** aberto. O novo campo será adicionado à coleção **Fields** do objeto **Record**. Se **Record** tiver sido derivado de um **Recordset**, o novo campo não será exibido na coleção **Fields** do objeto **Recordset**.

Um campo não-existente pode ser criado e acrescentado à coleção **Fields** atribuindo um valor ao objeto de campo como se ele já existisse na coleção. A atribuição disparará a criação e o acréscimo automático do objeto **Field** e, em seguida, será concluída.

Após acrescentar um **Field** à coleção **Fields** de um objeto **Record**, chame o método **Update** da coleção **Fields** para salvar a alteração.

