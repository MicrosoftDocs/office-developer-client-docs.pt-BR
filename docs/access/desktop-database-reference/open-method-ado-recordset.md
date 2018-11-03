---
title: Método Open (Recordset do ADO)
TOCTitle: Open method (ADO Recordset)
ms:assetid: 87ef19a4-28e1-dec7-ed33-4ae500b9c460
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249591(v=office.15)
ms:contentKeyID: 48546119
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a753ea57fba54f2e3b1a08c93f1309259f712446
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947704"
---
# <a name="open-method-ado-recordset"></a>Método Open (Recordset do ADO)


**Aplica-se a**: Access 2013, o Office 2013


Abre um cursor.

## <a name="syntax"></a>Sintaxe

*conjunto de registros*. Abra o*código-fonte*, *ActiveConnection*, *CursorType*, *LockType*, *Opções*

## <a name="parameters"></a>Parâmetros

  - *Source*

  - Opcional. Uma **Variant** que é avaliada para um objeto [Command](command-object-ado.md) válido, uma instrução SQL, um nome de tabela, uma chamada a procedimento armazenado, uma URL ou o nome de um arquivo ou objeto [Stream](stream-object-ado.md) que contém um [Recordset](recordset-object-ado.md) armazenado persistentemente.

  - *ActiveConnection*

  - Opcional. Uma **Variant** que é avaliada para um nome de variável de objeto [Connection](connection-object-ado.md) válido ou uma **String** que contém parâmetros [ConnectionString](connectionstring-property-ado.md).

  - *CursorType*

  - Opcional. Um valor [CursorTypeEnum](cursortypeenum.md) que determina o tipo de cursor que o provedordeve utilizar ao abrir o **Recordset**. O valor padrão é **adOpenForwardOnly**.

  - *LockType*

  - Opcional. Um valor [LockTypeEnum](locktypeenum.md) que determina qual tipo de bloqueio (simultaneidade) o provedor deve utilizar ao abrir o **Recordset**. O valor padrão é **adLockReadOnly**.

  - *Options*

  - Opcional. Um valor **Long** que indica como o provedor deverá avaliar o argumento *Source* se ele representar algo diferente de um objeto **Command** ou **Recordset** deve ser restaurado a partir de um arquivo onde ele foi salvo anteriormente. Pode ser um ou mais valores [CommandTypeEnum](commandtypeenum.md) ou [ExecuteOptionEnum](executeoptionenum.md), que podem ser combinados com um operador AND ciente de bit.


> [!NOTE]
> <P>[!OBSERVAçãO] Se você abrir um <STRONG>Recordset</STRONG> a partir de um <STRONG>Stream</STRONG> que contém um <STRONG>Recordset</STRONG> persistido, a utilização de um valor <STRONG>adAsyncFetchNonBlocking</STRONG> de <STRONG>ExecuteOptionEnum</STRONG> não terá efeito algum; a busca será síncrona e bloqueada.</P>



Os valores **adExecuteNoRecords** ou **adExecuteStream** de **ExecuteOpenEnum** não devem ser utilizados com **Open**.

## <a name="remarks"></a>Comentários

O cursor padrão para um **Recordset** do ADO é um cursor apenas leitura e apenas de avanço localizado no servidor.

A utilização do método **Open** em um objeto **Recordset** abre um cursor que representa registros de uma tabela base, os resultados de uma consulta ou um **Recordset** anteriormente salvo.

Use o argumento opcional de *origem* para especificar uma fonte de dados usando um dos seguintes: uma variável de objeto de **comando** , uma instrução SQL, um procedimento armazenado, um nome de tabela, uma URL ou um nome de caminho completo do arquivo. Se a *fonte* é um nome de caminho do arquivo, ele pode ser um caminho completo ("c:\\dir\\file.rst"), um caminho relativo ("… \\file.rst "), ou uma URL ("https://files/file.rst").

Não é recomendável usar o argumento *Source* do método **Open** para executar uma consulta ação que não retorna registros porque não há nenhuma maneira fácil de determinar se a chamada foi bem-sucedida. O **Recordset** retornado por tal consulta será fechado. Chame o método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) de um objeto **Command** ou o método [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) de um objeto **Connection** em vez de executar uma consulta que, tal como uma instrução SQL INSERT, não retorna registros.

O argumento *ActiveConnection* corresponde à propriedade [ActiveConnection](activeconnection-property-ado.md) e especifica em qual conexão para abrir o **Recordset** do objeto. Se você passar uma definição de conexão para esse argumento, o ADO abrirá uma nova conexão utilizando os parâmetros especificados. Depois de abrir o **Recordset** com um cursor do cliente (**CursorLocation** = **adUseClient**), você pode alterar o valor dessa propriedade para enviar atualizações para outro provedor. Ou ainda, poderá definir essa propriedade como **Nothing** (no Microsoft Visual Basic) ou NULL para desconectar o **Recordset** de qualquer provedor. No entanto, alterar **ActiveConnection** para um cursor do servidor gera um erro.

Para os demais argumentos que correspondem diretamente às propriedades de um objeto **Recordset** (*Source*, *CursorType* e *LockType*), a relação dos argumentos com as propriedades é a seguinte:

  - A propriedade é de leitura/gravação antes do objeto **Recordset** ser aberto.

  - As definições da propriedade são utilizadas, a menos que você passe os argumentos correspondentes ao executar o método **Open**. Se você passar um argumento, ele sobrescreverá a definição de propriedade correspondente, que será atualizada com o valor do argumento.

  - Depois de abrir o objeto **Recordset**, essas propriedades serão somente leitura.


> [!NOTE]
> <P>[!OBSERVAçãO] A propriedade <STRONG>ActiveConnection</STRONG> é apenas leitura para objetos <STRONG>Recordset</STRONG> cuja propriedade <A href="source-property-ado-recordset.md">Source</A> esteja definida para um objeto <STRONG>Command</STRONG> válido, mesmo se o objeto <STRONG>Recordset</STRONG> não estiver aberto.</P>



Se você passa um objeto **Command** do argumento de *origem* e também passa um argumento *ActiveConnection* , ocorrerá um erro. A propriedade **ActiveConnection** do objeto **Command** já deve estar definida para um objeto **Connection** válido ou uma sequência de conexão.

Se você passar algo que não seja um objeto **Command** do argumento de *origem* , você pode usar o argumento *Options* para otimizar a avaliação do argumento *Source* . Se o argumento *Options* não estiver definido, você pode enfrentar diminuição do desempenho porque ADO deve fazer chamadas para o provedor para determinar se o argumento é uma instrução SQL, um procedimento armazenado, uma URL ou um nome de tabela. Se você souber que tipo de *fonte* você estiver usando, definir o argumento *Options* instrui o ADO vá diretamente para o código relevante. Se o argumento *Options* não coincide com o tipo de *fonte* , ocorrerá um erro.

Se você passar um objeto **Stream** no argumento *Source* , você não deve passar informações para os demais argumentos. Fazer isso gerará um erro. As informações de **ActiveConnection** não são retidas quando um **Recordset** é aberto a partir de um **Stream**.

O padrão para o argumento *Options* é **adCmdFile** se nenhuma conexão estiver associado com o **Recordset**. Normalmente, esse será o caso para objetos **Recordset** armazenados persistentemente.

Se a fonte de dados não retornar registros, o provedor definirá as propriedades [BOF](bof-eof-properties-ado.md) e [EOF](bof-eof-properties-ado.md) para **True** e a posição do registro atual será indefinida. Ainda será possível adicionar novos dados a esse objeto **Recordset** vazio se o tipo do cursor assim o permitir.

Quando concluir as operações em um objeto **Recordset** aberto, utilize o método [Close](close-method-ado.md) para liberar quaisquer recursos associados do sistema. O fechamento de um objeto não o remove da memória; é possível alterar as definições de propriedade e utilizar o método **Open** para abri-lo novamente mais tarde. Para eliminar completamente um objeto da memória, defina a variável do objeto como *Nothing*.

Antes que a propriedade **ActiveConnection** seja definida, chame **Open** sem operandos para criar uma instância de um **Recordset** criado por campos acrescentados à coleção [Fields](fields-collection-ado.md) de **Recordset** .

Se você definiu a propriedade [CursorLocation](cursorlocation-property-ado.md) como **adUseClient**, poderá recuperar linhas assincronamente em uma das duas formas a seguir. O método recomendado é definir *Opções* para **adAsyncFetch**. De modo alternativo, é possível utilizar a propriedade dinâmica "Asynchronous Rowset Processing" na coleção [Properties](properties-collection-ado.md), mas os eventos relacionados recuperados poderão ser perdidos se você não definir o parâmetro **Options** como **adAsyncFetch**.


> [!NOTE]
> <P>Plano de fundo busca no provedor MS Remote é suportada apenas por meio do parâmetro de <EM>Options</EM> do método <STRONG>Open</STRONG> .</P>


> [!NOTE]
> [!OBSERVAçãO] URLs que utilizem o esquema http chamarão automaticamente o [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obter mais informações, consulte [URLs absolutas e relativas](absolute-and-relative-urls.md).


