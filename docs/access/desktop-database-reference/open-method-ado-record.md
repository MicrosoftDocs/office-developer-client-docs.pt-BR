---
title: Método Open (Record do ADO)
TOCTitle: Open Method (ADO Record)
ms:assetid: ba71c5c7-326e-d3b6-0e74-e8343ee6896f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249896(v=office.15)
ms:contentKeyID: 48547371
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f29f707f02ed8adbf2b1881b0721ce912b278353
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605825"
---
# <a name="open-method-ado-record"></a>Método Open (Record do ADO)


**Aplica-se a**: Access 2013 | Office 2013


Abre um objeto [Record](record-object-ado.md) existente ou cria um novo item representado pelo **Record** (tal como um arquivo ou diretório).

## <a name="syntax"></a>Sintaxe

Abra a *fonte*, *ActiveConnection*, *modo*, *CreateOptions*, *Opções*, *nome de usuário*, *senha*

## <a name="parameters"></a>Parâmetros

  - *Source*

  - Opcional. Uma **Variant** que pode representar a URL da entidade a ser representada por esse objeto **Record**, um **Command**, um [Recordset](recordset-object-ado.md) aberto ou outro objeto **Record**, uma sequência que contém uma instrução SQL SELECT ou um nome de tabela.

  - *ActiveConnection*

  - Opcional. Uma **Variant** que representa a sequência de conexão ou objeto [Connection](connection-object-ado.md) aberto.

  - *Mode*

  - Opcional. Um valor [ConnectModeEnum](connectmodeenum.md), cujo valor padrão é **adModeUnknown**, que especifica o modo de acesso para o objeto **Record** resultante.

  - *CreateOptions*

  - Opcional. Um valor [RecordCreateOptionsEnum](recordcreateoptionsenum.md), cujo valor padrão é **adFailIfNotExists**, que especifica se um arquivo ou diretório existente deve ser aberto ou se um novo arquivo ou diretório deve ser criado. Se definido para o valor padrão, o modo de acesso será obtido da propriedade [Mode](mode-property-ado.md). Esse parâmetro é ignorado quando o parâmetro *Source* não contém uma URL.

  - *Options*

  - Opcional. Um valor [RecordOpenOptionsEnum](recordopenoptionsenum.md), cujo valor padrão é **adOpenRecordUnspecified**, que especifica opções para a abertura do **Record**. Esses valores podem ser combinados.

  - *UserName*

  - Opcional. Um valor **String** que contém o ID de usuário que, se necessário, autoriza acesso a *Source*.

  - *Password*

  - Opcional. Um valor **String** que contém a senha que, se necessária, verifica *UserName*.

## <a name="remarks"></a>Comentários

*Source* pode ser:

  - Uma URL. Se o protocolo da URL for http, o Provedor de Internet será chamado por padrão. Se a URL apontar para um nó que contenha um script executável (tal como uma página .ASP), um **Record** que contém a fonte, em vez do conteúdo executado, será aberto por padrão. Use o argumento *Options* para modificar esse comportamento.

  - Um objeto **Record**. Um objeto **Record** aberto a partir de outro **Record** clonará o objeto **Record** original.

  - Um objeto **Command**. O objeto **Record** aberto representa a única linha retornada pela execução de **Command**. Se os resultados contiverem mais de uma única linha, o conteúdo da primeira linha será colocado no registro e um erro poderá ser adicionado à coleção **Errors**.

  - Uma instrução SQL SELECT. O objeto **Record** aberto representa a única linha retornada pela execução do conteúdo da sequência. Se os resultados contiverem mais de uma única linha, o conteúdo da primeira linha será colocado no registro e um erro poderá ser adicionado à coleção **Errors**.

  - O nome de uma tabela.

Se o objeto **Record** representar uma entidade que não pode ser acessada com uma URL (por exemplo, uma linha de um **Recordset** derivada de um banco de dados), os valores da propriedade [ParentURL](parenturl-property-ado.md) e do campo acessado com a constante **adRecordURL** serão nulos.


> [!NOTE]
<<<<<<< Cabeça
> <P>[!OBSERVAçãO] URLs que utilizem o esquema http chamarão automaticamente o <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. Para obter mais informações, consulte <A href="absolute-and-relative-urls.md">URLs Absolutas e Relativas</A>.</P>
=======
> [!OBSERVAçãO] URLs que utilizem o esquema http chamarão automaticamente o [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obter mais informações, consulte [URLs absolutas e relativas](absolute-and-relative-urls.md).
>>>>>>> mestre


