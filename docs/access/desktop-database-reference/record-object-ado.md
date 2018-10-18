---
title: Objeto Record (ADO)
TOCTitle: Record Object (ADO)
ms:assetid: 817aaf13-78d4-1134-aa94-997e92077c22
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249557(v=office.15)
ms:contentKeyID: 48545952
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 806b2292b12bededd299a0ef628601589afe0ce9
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603137"
---
# <a name="record-object-ado"></a>Objeto Record (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Representa uma linha de um [Recordset](recordset-object-ado.md) ou do provedor de dados ou um objeto retornado pelo provedor de dados semi-estruturado, como um arquivo ou diretório.

## <a name="remarks"></a>Comentários

Um objeto **Record** representa uma linha de dados e tem algumas similaridades conceituais com o **Recordset** de uma linha. Dependendo das capacidades do provedor, os objetos **Record** podem ser retornados diretamente do provedor, em vez de serem retornados do **Recordset** de uma linha, quando, por exemplo, é executada uma consulta SQL que seleciona somente uma linha; ou o objeto **Record** pode ser obtido diretamente de um objeto **Recordset**; ou um **Record** pode ser retornado diretamente de um provedor de dados semi-estruturados como o Microsoft Exchange OLE DB provider.

Você pode exibir os campos associados ao objeto **Record** por meio da coleção [Fields](fields-collection-ado.md) no objeto **Record**. O ADO permite colunas com valor de objeto, incluindo **Recordset**, **SafeArray** e valores escalares na coleção **Fields** dos objetos **Record**.

Se o objeto **Record** representar uma linha em um **Recordset**, será possível retornar para esse **Recordset** original com a propriedade [Source](source-property-ado-record.md).

O objeto **Record** também pode ser usado pelos provedores de dados semi-estruturados como o [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) para modelar os espaços para nome em forma de árvore. Cada nó em uma árvore é um objeto **Record** com as colunas associadas. As colunas podem representar os atributos desse nó e outras informações relevantes. O objeto **Record** pode representar tanto um nó folha como um nó não folha na estrutura em árvore. Os nós não folha têm outros nós como seus conteúdos enquanto os nós folha não têm esses conteúdos. Geralmente, os nós folha contêm fluxos de dados binários enquanto os nós não folha também têm um fluxo binário padrão associado. As propriedades do objeto **Record** identificam o tipo de nó.

O objeto **Record** também representa uma forma alternativa de navegar hierarquicamente nos dados organizados. É possível criar um objeto **Record** para representar a raiz de uma subárvore em uma estrutura em árvore grande e os novos objetos **Record** podem ser abertos para representar nós filhos.

Um recurso (por exemplo, um arquivo ou um diretório) pode ser identificado exclusivamente por uma URL absoluta. Um objeto [Connection](connection-object-ado.md) será criado e definido de forma implícita como o objeto **Record**, quando o **Record** for aberto com uma URL absoluta. Um objeto **Connection** pode ser definido de forma implícita como o objeto **Record** por meio da propriedade [ActiveConnection](activeconnection-property-ado.md). Os arquivos e diretórios acessíveis através do objeto de **Conexão** definem o *contexto* no qual as operações de **registro** podem ocorrer.

A modificação dos dados e os métodos de navegação no objeto **Record** também aceitam uma URL relativa, que localiza um recurso usando uma URL absoluta ou o contexto do objeto **Connection** como um ponto de partida.

<<<<<<< Cabeça

> [!NOTE]
> <P>[!OBSERVAçãO] URLs que utilizem o esquema http chamarão automaticamente o <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. Para obter mais informações, consulte <A href="absolute-and-relative-urls.md">URLs Absolutas e Relativas</A>.</P>
=======
> [!NOTE]
> [!OBSERVAçãO] URLs que utilizem o esquema http chamarão automaticamente o [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obter mais informações, consulte [URLs absolutas e relativas](absolute-and-relative-urls.md).
>>>>>>> mestre



Um objeto **Connection** está associado a cada objeto **Record**. Por esse motivo, as operações do objeto **Record** podem fazer parte de uma operação pela chamada dos métodos de transação do objeto **Connection**.

O objeto **Record** não oferecer suporte aos eventos ADO e, por esse motivo, não responderá às notificações.

Com os métodos e as propriedades de um objeto **Record**, é possível fazer o seguinte:

  - Definir ou retornar o objeto **Connection** associado à propriedade [ActiveConnection](activeconnection-property-ado.md).

  - Indicar as permissões de acesso à propriedade [Mode](mode-property-ado.md).

  - Retornar a URL do diretório, se houver, que contém o recurso representado pelo **Record** com a propriedade [ParentURL](parenturl-property-ado.md).

  - Indicar a URL absoluta, a URL relativa ou o **Recordset** a partir do qual o **Record** é derivado com a propriedade [Source](source-property-ado-record.md).

  - Indicar o status atual do **Record** com a propriedade [State](state-property-ado.md).

  - Indicar o tipo de **Record** — *simples*, *coleção* ou *documento estruturado* — com a propriedade [RecordType](recordtype-property-ado.md).

  - Suspender a execução de uma operação assíncrona com o método [Cancel](cancel-method-ado.md).

  - Desassociar o **Record** de uma fonte de dados com o método [Close](close-method-ado.md).

  - Copiar o arquivo ou o diretório representado por um **Record** para outro local com o método [CopyRecord](copyrecord-method-ado.md).

  - Excluir o arquivo ou o diretório e os subdiretórios, representado por um **Record** com o método [DeleteRecord](deleterecord-method-ado.md).

  - Abrir um **Recordset** contendo linhas que representam os subdiretórios e os arquivos da entidade representados pelo **Record** com o método [GetChildren](getchildren-method-ado.md).

  - Mover (renomear) o arquivo ou o diretório e os subdiretórios, representado por um **Record** para outro local com o método [MoveRecord](moverecord-method-ado.md).

  - Associar o **Record** com uma fonte de dados existente ou criar um novo arquivo ou diretório com o método [Open](open-method-ado-record.md).

