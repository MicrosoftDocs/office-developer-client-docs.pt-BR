---
title: Detalhes do HelloData (referência do banco de dados da área de trabalho do Access)
TOCTitle: HelloData details
ms:assetid: db51e15c-1b5b-c64a-2f84-34dd0e78c6cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250105(v=office.15)
ms:contentKeyID: 48548103
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 78b04b74d4e2b8d9c215235d6e7ccebed4fa2ef2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291996"
---
# <a name="hellodata-details"></a>Detalhes do HelloData


**Aplica-se ao:** Access 2013, Office 2013

O aplicativo HelloData passa por todas as operações básicas de um aplicativo típico do ADO: obter, examinar, editar e atualizar dados. Ao iniciar o aplicativo, clique no primeiro botão, **Get Data**. Isso executará a sub-rotina GetData().

## <a name="getdata"></a>GetData

GetData coloca uma sequência de conexão válida em uma variável de nível de módulo, *m \_ sConnStr*. Para obter mais informações sobre sequências de conexão, consulte [Criando a sequência de conexão](creating-the-connection-string.md).

Use uma instrução **OnError** do Visual Basic para atribuir um manipular de erros. Para obter mais informações sobre o tratamento de erros no ADO, consulte o [Capítulo 6: tratamento de erros](chapter-6-error-handling.md). Um novo objeto **Connection** é criado e a propriedade **CursorLocation** é definida como **adUseClient**, pois o exemplo HelloData cria um *Recordset desconectado*. Isto significa que depois que os dados forem encontrados na fonte de dados, a conexão física com a fonte de dados será interrompida, mas você poderá continuar trabalhando com os dados, que serão armazenados localmente em cache no seu objeto **Recordset**.

Depois que a conexão for aberta, atribua uma cadeia de caracteres SQL a uma variável (sSQL). Em seguida, insinue um novo **objeto Recordset,** m \_ oRecordset1 . Na próxima linha de código, abra **o Recordset** sobre a **conexão existente,** passando. Na próxima linha de código, abra **o Recordset** sobre o **Connection** existente , passando sSQL como a origem do **Recordset**. Para ajudar o ADO a determinar que a cadeia de caracteres SQL que você passou como fonte de **Recordset** é uma definição textual de um comando, você passará **adCmdText** no argumento final do método **Open** de **Recordset**. Essa linha também define o **LockType** e o **CursorType** associados ao **Recordset**.

A próxima linha do código iguala as propriedades **MarshalOptions** e **adMarshalModifiedOnly**. **MarshalOptions** indica quais registros devem ser empacotados para a camada intermediária (ou servidor Web). Para obter mais informações sobre o empacotamento, consulte a documentação do COM. Ao usar **adMarshalModifiedOnly** com um cursor do lado do cliente ([CursorLocation](cursorlocation-property-ado.md)  =  **adUseClient**), somente os registros que foram modificados no cliente são gravados de volta na camada intermediária. Definir **MarshalOptions** como **adMarshalModifiedOnly** pode melhorar o desempenho, pois menos linhas são empacotadas.

Em seguida, desconecte o **Recordset** igualando as propriedades **ActiveConnection** e **Nothing**. Para obter mais informações, consulte [Desconectando e reconectando o Recordset](disconnecting-and-reconnecting-the-recordset.md) no Capítulo 5: atualizando e mantendo a persistência de dados.

Feche a conexão com a fonte de dados e destrua o objeto **Connection** existente para liberar os recursos que ele consumia.

A etapa final é definir o **Recordset** como **DataSource** para o Microsoft DataBound Grid Control no formulário, de modo que você possa exibir facilmente os dados do **Recordset** no formulário.

Clique no segundo botão, **Examine Data**. Isso executará a sub-rotina ExamineData.

## <a name="examinedata"></a>ExamineData

ExamineData utiliza vários métodos e propriedades do objeto **Recordset** para exibir informações sobre os dados do **Recordeset**. Para relatar o número de registros, ela usa a propriedade **RecordCount**. Ela executa um loop por meio do **Recordset** e imprime o valor da propriedade **AbsolutePosition** na caixa de exibição de texto do formulário. Além disso, ainda durante o loop, o valor da propriedade **Bookmark** do terceiro registro é colocado em uma variável variante, *vBookmark*, para uso posterior.

A rotina navega diretamente de volta ao terceiro registro usando a variável indicadora que a armazenou antes. A rotina chama a sub-rotina WalkFields, que executa um loop por meio da coleção **Fields** do **Recordset** e exibe detalhes de cada **Field** existente na coleção.

Finalmente, ExamineData usa a propriedade **Filter** do **Recordset** para filtrar exclusivamente os registros com CategoryId igual a 2. O resultado da aplicação desse filtro é imediatamente visível na grade de exibição do formulário.

Para obter mais informações sobre a funcionalidade mostrada na sub-rotina ExamineData, consulte o [Capítulo 3: examinando dados](chapter-3-examining-data.md).

Em seguida, clique no terceiro botão, **Edit Data**. Isso executará a sub-rotina EditData.

## <a name="editdata"></a>EditData

Quando o código chega à sub-rotina EditData, o **Recordset** ainda está filtrado com base em CategoryId igual a 2 e, portanto, somente os itens que atendem aos critérios do filtro estão visíveis. Inicialmente, o código executa um loop por meio do **Recordset** e aumenta o preço de cada item visível do **Recordset** em 10%. Para mudar o valor do campo **Price**, a propriedade **Value** desse campo deve ser definida como igual a uma nova quantia válida.

Lembre-se de que o **Recordset** está desconectado da fonte de dados. As alterações feitas em EditData afetam somente a cópia dos dados armazenada no cache local. Para obter mais informações, consulte o [Capítulo 4: editando dados](chapter-4-editing-data.md).

As alterações só serão aplicadas à fonte de dados quando você clicar no quarto botão, **Update Data**. Isso executará a sub-rotina UpdateData.

## <a name="updatedata"></a>UpdateData

Inicialmente, UpdateData remove o filtro que foi aplicado ao **Recordset**. O código remove e redefine como **o DataSource** para o Microsoft Bound DataGrid no formulário para que o **Recordset** não filtrado apareça na grade.

Em seguida, o código verifica se você pode retroceder no **Recordset** usando o método **Supports** com o argumento **adMovePrevious**.

A rotina move-se para o primeiro registro usando o método **MoveFirst** e exibe os valores original e atual do campo usando as propriedades **OriginalValue** e **Value** do objeto **Field**. Essas propriedades, juntamente com a propriedade **UnderlyingValue** (não utilizada aqui), são discutidas no [Capítulo 5: atualizando e mantendo a persistência de dados](chapter-5-updating-and-persisting-data.md).

Em seguida, um novo objeto **Connection** é criado e usado para restabelecer uma conexão com a fonte de dados. Para reconectar o **Recordset** à fonte de dados, o novo **Connection** é definido como **ActiveConnection** no **Recordset**. Para enviar as atualizações para o servidor, o código chama o método **UpdateBatch** no **Recordset**.

Se a atualização em lotes for bem-sucedida, uma variável de sinalizador de nível de módulo será definida como True. Mais adiante, isto servirá para lembrá-lo de limpar todas as alterações feitas no banco de dados.

Finalmente, o código volta ao primeiro registro do **Recordset** e exibe os valores originais e atuais. Os valores são os mesmos após a chamada de **UpdateBatch**.

Para obter informações mais detalhadas sobre a atualização de dados, inclusive o que fazer se os dados no servidor forem alterados enquanto o seu **Recordset** estiver desconectado, consulte o [Capítulo 5: atualizando e mantendo a persistência de dados](chapter-5-updating-and-persisting-data.md).

## <a name="form_unload"></a>Descarregar \_ Formulário

A \_ sub-rotina Descarregar Formulário é importante por vários motivos. Primeiro, como este é um aplicativo de exemplo, o Form Unload limpa as alterações feitas no banco de dados \_ antes de o aplicativo sair. Em segundo lugar, o código mostra como o método **Execute** pode ser usado para executar um comando diretamente a partir de um objeto **Connection** aberto. Finalmente, ele mostra um exemplo da execução de uma consulta à fonte de dados sem retorno de linhas (uma consulta UPDATE).

