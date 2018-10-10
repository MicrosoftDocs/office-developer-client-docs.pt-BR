---
title: Propriedade ActiveConnection (ADO)
TOCTitle: ActiveConnection Property (ADO)
ms:assetid: 5501b2d7-b62c-5fff-1edd-2b7efb3f8c4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249281(v=office.15)
ms:contentKeyID: 48544918
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231115
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d44a17d192abdb68755a2010184b4fb4d6531174
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465391"
---
# <a name="activeconnection-property-ado"></a>Propriedade ActiveConnection (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Indica a qual objeto [Connection](connection-object-ado.md) pertence o objeto [Command](command-object-ado.md), [Recordset](recordset-object-ado.md) ou [Record](record-object-ado.md).

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Configura ou retorna um valor **String** contendo uma definição para uma conexão, caso a conexão esteja fechada, ou um **Variant** contendo o objeto **Connection** atual no caso de a conexão estar aberta. O padrão é uma referência nula ao objeto. Consulte também a propriedade [ConnectionString](connectionstring-property-ado.md).

## <a name="remarks"></a>Comentários

Use a propriedade **ActiveConnection** para determinar o objeto **Connection** no qual o objeto **Command** especificado será executado ou o objeto **Recordset** especificado será aberto.

**Command**

Para os objetos **Command**, a propriedade **ActiveConnection** é leitura/gravação.

Ocorrerá um erro se você tentar chamar o método [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) em um objeto **Command** antes de configurar essa propriedade como um objeto **Connection** aberto ou uma sequência de conexão válida.

**Microsoft Visual Basic** Configurar a propriedade **ActiveConnection** como *Nothing* desassocia o objeto **Command** da **Conexão** atual e faz com que o provedor liberar quaisquer recursos associados na fonte de dados. Assim, você pode associar o objeto **Command** ao mesmo objeto **Connection** ou a um outro. Alguns provedores permitem que você altere a configuração da propriedade de uma **Conexão** para outra, sem precisar primeiro definir a propriedade como *Nothing*.

Se a coleção [Parameters](parameters-collection-ado.md) do objeto **Command** contiver parâmetros fornecidos pelo provedor, a coleção está desmarcada, se você definir a propriedade **ActiveConnection** como *Nothing* ou para outro objeto de **Conexão** . Se você cria objetos [Parameter](parameter-object-ado.md) e usá-los para preencher a coleção **Parameters** do objeto **Command** manualmente, definindo o **ActiveConnection** como *Nothing* ou para outro objeto de **Conexão** de propriedade deixa a coleção **Parameters** intacta.

O fechamento de um objeto **Connection** ao qual um objeto **Command** está associado define a propriedade **ActiveConnection** como *Nothing*. A definição dessa propriedade para um objeto **Connection** fechado gera um erro.

**Recordset**

Para objetos **Recordset** abertos ou para objetos **Recordset** cuja propriedade [Source](source-property-ado-recordset.md) esteja definida como um objeto **Command** válido, a propriedade **ActiveConnection** é somente leitura. Caso contrário, ela é leitura/gravação.

Você pode definir essa propriedade como um objeto **Connection** válido ou como uma sequência de conexão válida. Neste caso, o provedor cria um novo objeto **Connection** usando essa definição e abre a conexão. Além disso, o provedor pode definir essa propriedade para o novo objeto **Connection** de modo que você acesse o objeto **Connection** para obter informações de erro estendidas ou execute outros comandos.

Se você usar o argumento *ActiveConnection* do método [Open](open-method-ado-recordset.md) para abrir um objeto **Recordset** , a propriedade **ActiveConnection** herdará o valor do argumento.

Se você configurar a propriedade **Source** do objeto **Recordset** como uma variável de objeto **Command** válida, a propriedade **ActiveConnection** do **Recordset** herdará a definição da propriedade **ActiveConnection** do objeto **Command**.

**Uso de serviço de dados remotos** Quando usado em um objeto Recordset do lado do cliente, essa propriedade pode ser definida apenas como uma sequência de conexão ou (no Microsoft Visual Basic ou Visual Basic, Scripting Edition) como *Nothing*.

**Record**

Essa propriedade é leitura/gravação quando o objeto **Record** estiver fechado, podendo conter uma sequência de conexão ou referência a um objeto **Connection** aberto. Ela é somente leitura quando o objeto **Record** estiver aberto e contiver uma referência a um objeto **Connection** aberto.

Um objeto **Connection** é criado implicitamente quando o objeto **Record** é aberto a partir de uma URL. Abra o **Record** com um objeto **Connection** existente e aberto atribuindo o objeto **Connection** a essa propriedade ou usando o objeto **Connection** como um parâmetro na chamada do método [Open](open-method-ado-record.md). Se o **Record** for aberto a partir de um **Record** ou [Recordset](recordset-object-ado.md) existente, ele será automaticamente associado ao objeto **Connection** do objeto **Record** ou **Recordset**.


> [!NOTE]
> <P>[!OBSERVAçãO] As URLs que usam o esquema http invocarão automaticamente o <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. Para obter mais informações, consulte <A href="absolute-and-relative-urls.md">URLs absolutas e relativas</A>.</P>


