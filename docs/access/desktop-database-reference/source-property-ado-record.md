---
title: Propriedade Source (Record do ADO)
TOCTitle: Source Property (ADO Record)
ms:assetid: f36f0f5f-4493-d8c5-db4b-c72f5031bcb3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250235(v=office.15)
ms:contentKeyID: 48548670
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4d6e010ce8db93baaf8faddaeff5ab4dabda6a84
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603382"
---
# <a name="source-property-ado-record"></a>Propriedade Source (Record do ADO)


**Aplica-se a**: Access 2013 | Office 2013

Indica a fonte de dados ou o objeto representado pelo [Record](record-object-ado.md).

<<<<<<< Cabeça
## <a name="settings-and-return-values"></a>Configurações e valor de retorno
=======
## <a name="settings-and-return-values"></a>Configurações e valores de retorno
>>>>>>> mestre

Define ou retorna um valor **Variant** que indica a entidade representada pelo **Record**.

## <a name="remarks"></a>Comentários

A propriedade **Source** retorna o argumento de *fonte* do objeto **Record** do método [Open](open-method-ado-record.md) . Ela pode conter uma cadeia de caracteres de URL absoluta ou relativa. Uma URL absoluta pode ser utilizada sem a definição da propriedade [ActiveConnection](activeconnection-property-ado.md) para abrir diretamente o objeto **Record**. Neste caso, será criado um objeto **Connection** implícito.

A propriedade **Source** também pode conter uma referência a um **Recordset** já aberto, que abre um objeto **Record** representando a linha atual no **Recordset**.

A propriedade **Source** também pode conter uma referência a um objeto [Command](command-object-ado.md), que retorna uma única linha de dados do provedor.

Se a propriedade **ActiveConnection** também for definida, então a propriedade **Source** deverá apontar para algum objeto que exista dentro do escopo dessa conexão. Por exemplo, namespaces em árvore estruturada, se a propriedade **Source** contiver uma URL absoluta, ela deverá apontar para um nó que exista dentro do escopo do nó identificado pela URL na sequência de conexão. Se a propriedade **Source** contiver uma URL relativa, ela será validada no conjunto de contexto pela propriedade **ActiveConnection**.

A propriedade **Source** será leitura/gravação enquanto o objeto **Record** estiver fechado e somente leitura enquanto o objeto **Record** estiver aberto.

<<<<<<< Cabeça

> [!NOTE]
> <P>[!OBSERVAçãO] URLs que utilizem o esquema http chamarão automaticamente o <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. Para obter mais informações, consulte <A href="absolute-and-relative-urls.md">URLs Absolutas e Relativas</A>.</P>
=======
> [!NOTE]
> [!OBSERVAçãO] URLs que utilizem o esquema http chamarão automaticamente o [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obter mais informações, consulte [URLs absolutas e relativas](absolute-and-relative-urls.md).
>>>>>>> mestre


