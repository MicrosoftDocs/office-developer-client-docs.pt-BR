---
title: Método AddNew (ADO)
TOCTitle: AddNew Method (ADO)
ms:assetid: bae09be0-5707-4f38-9c74-0acd0f29dbac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249899(v=office.15)
ms:contentKeyID: 48547384
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b84e6651093d932a17ff20097841bf84bac00c66
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464944"
---
# <a name="addnew-method-ado"></a>Método AddNew (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Cria um novo registro para um objeto [Recordset](recordset-object-ado.md) atualizável.

## <a name="syntax"></a>Sintaxe

*conjunto de registros*. AddNew *FieldList*, *valores*

## <a name="parameters"></a>Parâmetros

  - *recordset*

  - Um objeto **Recordset**.

  - *FieldList*

  - Opcional. Um único nome, ou uma matriz de nomes ou posições ordinais dos campos no novo registro.

  - *Values*

  - Opcional. Um único valor, ou uma matriz de valores para os campos no novo registro. Se *Fieldlist* é uma matriz, os *valores* também deve ser uma matriz com o mesmo número de membros; Caso contrário, ocorrerá um erro. A ordem dos nomes de campo deve corresponder à ordem dos valores de campo em cada matriz.

## <a name="remarks"></a>Comentários

Use o método **AddNew** para criar e inicializar um novo registro. Use o método [Supports](supports-method-ado.md) com **adAddNew** (valor [CursorOptionEnum](cursoroptionenum.md)) para verificar se é possível adicionar registros ao objeto **Recordset** atual.

Depois que você chamar o método **AddNew**, o novo registro passará a ser o registro atual e permanecerá atual depois que o método [Update](update-method-ado.md) for chamado. Como o novo registro é acrescentado a **Recordset**, uma chamada para **MoveNext** após Update ultrapassará o fim de **Recordset**, tornando **EOF** True. Se o objeto **Recordset** não oferecer suporte a indicadores, você não poderá acessar o novo registro ao passar para outro. Dependendo do tipo de cursor, talvez seja necessário chamar o método [Requery](requery-method-ado.md) para tornar o novo registro acessível.

Se você chamar **AddNew** durante a edição do registro atual ou a adição de um novo registro, o ADO chamará o método **Update** para salvar as alterações e, em seguida, criará o novo registro.

O comportamento do método **AddNew** depende do modo de atualização do objeto **Recordset** e se serão passados os argumentos *Fieldlist* e *Values* .

No *modo de atualização imediato* (em que o provedor grava as alterações na fonte de dados subjacente quando você chama o método **Update**), se você chamar o método **AddNew** sem argumentos, a propriedade [EditMode](editmode-property-ado.md) será definida como **adEditAdd** (valor [EditModeEnum](editmodeenum.md)). O provedor armazena localmente em cache qualquer alteração de valor de campo. A chamada do método **Update** posta o novo registro no banco de dados e redefine a propriedade **EditMode** como  **adEditNone** (valor **EditModeEnum**). Se você passar os argumentos *Fieldlist* e *Values*, o ADO postará o novo registro imediatamente no banco de dados (nenhuma chamada de **Update** é necessária); o valor da propriedade **EditMode** não é alterado (**adEditNone**).

No *modo de atualização em lotes* (no qual o provedor caches várias alterações e grava-los à fonte de dados subjacente somente quando você chamar o método [UpdateBatch](updatebatch-method-ado.md) ), chamar o método **AddNew** sem argumentos define a **EditMode** propriedade para **adEditAdd**. O provedor armazena no cache local as alterações de valores de campo. A chamada do método **Update** adiciona o novo registro ao **Recordset** atual e redefine a propriedade **EditMode** em **adEditNone**, mas o provedor não posta as alterações no banco de dados subjacente até a chamada do método **UpdateBatch**. Se você passar os argumentos *Fieldlist* e *Values* , ADO envia o novo registro para o provedor de armazenamento em cache; Você precisará chamar o método **UpdateBatch** para lançar o novo registro no banco de dados subjacente.

