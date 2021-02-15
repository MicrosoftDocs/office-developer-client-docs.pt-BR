---
title: Método Open (Recordset do ADO)
TOCTitle: Open method (ADO Recordset)
ms:assetid: 87ef19a4-28e1-dec7-ed33-4ae500b9c460
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249591(v=office.15)
ms:contentKeyID: 48546119
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e5f8dbdfa61a671e2efb9aac2596cfda5cd1727b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288403"
---
# <a name="open-method-ado-recordset"></a>Método Open (Recordset do ADO)

**Aplica-se ao:** Access 2013, Office 2013

Abre um cursor.

## <a name="syntax"></a>Sintaxe

*recordset*. Open *Source*, *ActiveConnection*, *CursorType*, *LockType*, *Options*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Source* |Opcional. Uma **Variant** que é avaliada para um objeto [Command](command-object-ado.md) válido, uma instrução SQL, um nome de tabela, uma chamada a procedimento armazenado, uma URL ou o nome de um arquivo ou objeto [Stream](stream-object-ado.md) que contém um [Recordset](recordset-object-ado.md) armazenado persistentemente.|
|*ActiveConnection* |Opcional. Uma **Variant** que é avaliada para um nome de variável de objeto [Connection](connection-object-ado.md) válido ou uma **String** que contém parâmetros [ConnectionString](connectionstring-property-ado.md).|
|*CursorType* |Opcional. Um valor [CursorTypeEnum](cursortypeenum.md) que determina o tipo de cursor que o provedordeve utilizar ao abrir o **Recordset**. O valor padrão é **adOpenForwardOnly**.|
|*LockType* |Opcional. Um valor [LockTypeEnum](locktypeenum.md) que determina qual tipo de bloqueio (simultaneidade) o provedor deve utilizar ao abrir o **Recordset**. O valor padrão é **adLockReadOnly**.|
|*Options* |Opcional. Um valor **Long** que indica como o provedor deve avaliar o argumento *Source* se ele representar algo diferente de um objeto **Command** ou se o **Recordset** deve ser restaurado a partir de um arquivo em que ele foi salvo anteriormente. Pode ser um ou mais valores [CommandTypeEnum](commandtypeenum.md) ou [ExecuteOptionEnum](executeoptionenum.md), que podem ser combinados com um operador AND ciente de bit.|

> [!NOTE]
> [!OBSERVAçãO] Se você abrir um **Recordset** a partir de um **Stream** que contém um **Recordset** persistido, a utilização de um valor **adAsyncFetchNonBlocking** de **ExecuteOptionEnum** não terá efeito algum; a busca será síncrona e bloqueada.

Os valores **adExecuteNoRecords** ou **adExecuteStream** de **ExecuteOpenEnum** não devem ser utilizados com **Open**.

## <a name="remarks"></a>Comentários

O cursor padrão para um **Recordset** do ADO é um cursor apenas leitura e apenas de avanço localizado no servidor.

A utilização do método **Open** em um objeto **Recordset** abre um cursor que representa registros de uma tabela base, os resultados de uma consulta ou um **Recordset** anteriormente salvo.

Utilize o argumento opcional *Source* para especificar uma fonte de dados que utiliza um dos seguintes itens: uma variável de objeto **Command**, uma instrução SQL, um procedimento armazenado, um nome de tabela, uma URL ou um nome de caminho de arquivo completo. Se *Source* for um nome de caminho de arquivo, pode ser um caminho completo ("c: \\ dir \\ file.rst"), um caminho relativo (".. \\ file.rst") ou uma URL (" https://files/file.rst ").

Não é uma boa ideia utilizar o argumento *Source* do método **Open** para executar uma consulta ação que não retorna registros porque não existe uma forma fácil de determinar se a chamada obteve êxito. O **Recordset** retornado por tal consulta será fechado. Chame o método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) de um objeto **Command** ou o método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) de um objeto **Connection** em vez de executar uma consulta que, tal como uma instrução SQL INSERT, não retorna registros.

O argumento *ActiveConnection* corresponde à propriedade [ActiveConnection](activeconnection-property-ado.md) e especifica em qual conexão abrir o objeto **Recordset**. Se você passar uma definição de conexão para esse argumento, o ADO abrirá uma nova conexão utilizando os parâmetros especificados. Depois de abrir o **Recordset** com um cursor do lado do cliente (**CursorLocation**  =  **adUseClient**), você pode alterar o valor dessa propriedade para enviar atualizações para outro provedor. Ou ainda, poderá definir essa propriedade como **Nothing** (no Microsoft Visual Basic) ou NULL para desconectar o **Recordset** de qualquer provedor. No entanto, alterar **ActiveConnection** para um cursor do servidor gera um erro.

Para os demais argumentos que correspondem diretamente às propriedades de um objeto **Recordset** (*Source*, *CursorType* e *LockType*), a relação dos argumentos com as propriedades é a seguinte:

- A propriedade é de leitura/gravação antes do objeto **Recordset** ser aberto.

- As definições da propriedade são utilizadas, a menos que você passe os argumentos correspondentes ao executar o método **Open**. Se você passar um argumento, ele sobrescreverá a definição de propriedade correspondente, que será atualizada com o valor do argumento.

- Depois de abrir o objeto **Recordset**, essas propriedades serão somente leitura.

> [!NOTE]
> A propriedade **ActiveConnection** é apenas leitura para objetos **Recordset** cuja propriedade [Source](source-property-ado-recordset.md) esteja definida para um objeto **Command** válido, mesmo se o objeto **Recordset** não estiver aberto.

Se você passar um objeto **Command** no argumento *Source* e também passar um argumento *ActiveConnection*, ocorrerá um erro. A propriedade **ActiveConnection** do objeto **Command** já deve estar definida para um objeto **Connection** válido ou uma sequência de conexão.

Se você passar algo diferente de um objeto **Command** no argumento *Source*, poderá utilizar o argumento *Options* para otimizar a avaliação do argumento *Source*. Se o argumento *Options* não estiver definido, você poderá experimentar um desempenho diminuído porque o ADO deve fazer chamadas ao provedor para determinar se o argumento é uma instrução SQL, um procedimento armazenado, uma URL ou um nome de tabela. Se você souber qual tipo de *Source* está utilizando, a definição do argumento *Options* instrui o ADO a ir diretamente para o código relevante. Se o argumento *Options* não corresponder ao tipo de *Source*, ocorrerá um erro.

Se você passar um objeto **Stream** no argumento *Source*, não deverá passar informações para os demais argumentos. Fazer isso gerará um erro. As informações de **ActiveConnection** não são retidas quando um **Recordset** é aberto a partir de um **Stream**.

O padrão para o argumento *Options* é **adCmdFile** se nenhuma conexão estiver associada ao **Recordset**. Normalmente, esse será o caso para objetos **Recordset** armazenados persistentemente.

Se a fonte de dados não retornar registros, o provedor definirá as propriedades [BOF](bof-eof-properties-ado.md) e [EOF](bof-eof-properties-ado.md) para **True** e a posição do registro atual será indefinida. Ainda será possível adicionar novos dados a esse objeto **Recordset** vazio se o tipo do cursor assim o permitir.

Quando concluir as operações em um objeto **Recordset** aberto, utilize o método [Close](close-method-ado.md) para liberar quaisquer recursos associados do sistema. O fechamento de um objeto não o remove da memória; é possível alterar as definições de propriedade e utilizar o método **Open** para abri-lo novamente mais tarde. Para eliminar completamente um objeto da memória, defina a variável do objeto como *Nothing*.

Antes da **propriedade ActiveConnection** ser definida, chame **Open** sem operands para criar uma instância de um **Recordset** criado por campos de adição à coleção **Recordset** [Fields](fields-collection-ado.md) .

Se você definiu a propriedade [CursorLocation](cursorlocation-property-ado.md) como **adUseClient**, poderá recuperar linhas assincronamente em uma das duas formas a seguir. O método recomendado é definir *Options* como **adAsyncFetch**. De modo alternativo, é possível utilizar a propriedade dinâmica "Asynchronous Rowset Processing" na coleção [Properties](properties-collection-ado.md), mas os eventos relacionados recuperados poderão ser perdidos se você não definir o parâmetro **Options** como **adAsyncFetch**.

> [!NOTE]
> A busca em segundo plano no provedor MS Remote é suportada apenas por meio do parâmetro *Options* do método **Open**.

> [!NOTE]
> [!OBSERVAçãO] URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obter mais informações, consulte [URLs absolutas e relativas.](absolute-and-relative-urls.md)


