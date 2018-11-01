---
title: Objeto Error - ActiveX Data Objects (ADO)
TOCTitle: Error Object (ADO)
ms:assetid: 97e478bf-8b25-03a8-9358-abba5069cba3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249678(v=office.15)
ms:contentKeyID: 48546477
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ae89c4d2300b167a8e7b993ad8830838d91f0617
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877020"
---
# <a name="error-object-ado"></a>Objeto Error (ADO)


**Aplica-se a**: Access 2013, o Office 2013

Contém os detalhes sobre os erros de acesso aos dados que pertencem à uma única operação que envolve o provedor.

## <a name="remarks"></a>Comentários

Qualquer operação envolvendo os objetos ADO pode gerar um ou vários erros de provedor. À medida que cada erro ocorrer, um ou vários objetos **Error** serão colocados na coleção [Errors](errors-collection-ado.md) do objeto [Connection](connection-object-ado.md). Quando a operação do ADO gerar um erro, a coleção **Errors** será limpa e o novo conjunto de objetos **Error** será colocado na coleção **Errors**.

> [!NOTE]
> [!OBSERVAçãO] Cada objeto **Error** representa um erro de provedor específico e não um erro do ADO. Os erros do ADO são apresentados no mecanismo de tratamento de exceções do tempo de execução. Por exemplo, no Microsoft Visual Basic, a ocorrência de um erro específico de ADO disparará um evento **On Error** e aparecerá no objeto **Error**. Para obter uma lista completa dos erros do ADO, consulte o tópico [ErrorValueEnum](errorvalueenum.md).

Leia as propriedades do objeto **Error** para obter os detalhes específicos sobre cada erro, incluindo o seguinte:

- A propriedade [Description](description-property-ado.md), que contém o texto do erro. Esta é a propriedade padrão.

- A propriedade [Number](number-property-ado.md), que contém o valor inteiro **Long** da constante de erro.

- A propriedade [Source](source-property-ado-error.md), que identifica o objeto que causou o erro. Isso será particularmente útil quando você tiver vários objetos **Error** na coleção **Errors** depois de uma solicitação de uma fonte de dados.

- As propriedades [SQLState](sqlstate-property-ado.md) e [NativeError](nativeerror-property-ado.md) que fornecem informações a partir das fontes de dados SQL.

Quando ocorrer um erro de provedor, este será colocado na coleção **Errors** do objeto **Connection**. O ADO suporta o retorno de vários erros ocasionados uma única operação do ADO para levar em conta as informações específicas do erro para o provedor. Para obter essas valiosas informações do erro em um manipulador de erros, use os recursos adequados para a interceptação de erros do idioma ou do ambiente no qual você estiver trabalhando e depois use os loops aninhados para enumerar as propriedades de cada objeto **Error** na coleção **Errors**.

**Microsoft Visual Basic e usuários do VBScript** Se não houver nenhum objeto de **Conexão** válido, você precisará recuperar informações de erro do objeto **Error** .

Exatamente como os provedores fazem, o ADO limpa o objeto **OLE Error Info** antes de fazer uma chamada que poderia gerar potencialmente um novo erro de provedor. No entanto, a coleção **Errors** no objeto **Connection** será limpa e preenchida somente quando o provedor gerar um novo erro ou quando o método [Clear](clear-method-ado.md) for chamado.

Algumas propriedades e métodos retornam avisos que aparecem como objetos **Error** na coleção **Errors** mas não suspendem a execução de um programa. Antes de chamar os métodos [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) ou [CancelBatch](cancelbatch-method-ado.md) em um objeto [Recordset](recordset-object-ado.md), o método [Open](open-method-ado-connection.md) em um objeto **Connection** ou definir a propriedade [Filter](filter-property-ado.md) em um objeto **Recordset**, chame o método **Clear** na coleção **Errors**. Dessa forma, será possível ler a propriedade [Count](count-property-ado.md) da coleção **Errors** para verificar os avisos retornados.

