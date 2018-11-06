---
title: Objeto Stream (ADO)
TOCTitle: Stream object (ADO)
ms:assetid: d49b1514-e0b4-0aca-d5c2-8266f3f4fe65
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250065(v=office.15)
ms:contentKeyID: 48547945
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 75e0422b6c6fcd2f893777884d35bade81a793f6
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997039"
---
# <a name="stream-object-ado"></a>Objeto Stream (ADO)


**Aplica-se a**: Access 2013, o Office 2013

Representa um fluxo de dados ou texto binário.

## <a name="remarks"></a>Comentários

Em hierarquias estruturada em árvore como um sistema de arquivos ou um sistema de email, um [registro](record-object-ado.md) pode ter um fluxo de binário padrão de bits associados a ele que contém o conteúdo do arquivo ou email. Um objeto **Stream** pode ser usado para manipular campos ou registros que contenham esses fluxos de dados. Um objeto **Stream** pode ser obtido dessas formas:

  - A partir de uma URL que aponta para um objeto (geralmente um arquivo) que contenha dados binários ou de texto. Esse objeto pode ser um documento simples, um objeto **Record** que representa um documento estruturado ou uma pasta.

  - Pela abertura do objeto **Stream** padrão associado a um objeto **Record**. Obtenha o fluxo padrão associado ao objeto **Record**, quando **Record** estiver aberto, para eliminar um percurso circular apenas para abrir o fluxo.

  - Pelo instanciamento de um objeto **Stream**. Esses objetos **Stream** podem ser usados para armazenar dados no aplicativo. Ao contrário de um **Stream** associado a uma URL ou **Stream** padrão de um **Record**, um **Stream** instanciado não está associado a uma fonte base por padrão.

Com os métodos e as propriedades e um objeto **Stream**, você pode fazer o seguinte:

  - Abrir um objeto **Stream** a partir de um **Record** ou uma URL com o método [Open](open-method-ado-stream.md).

  - Fechar um **Stream** com o método [Close](close-method-ado.md).

  - Inserir bytes ou texto para um **Stream** com os métodos [Write](write-method-ado.md) e [WriteText](writetext-method-ado.md).

  - Ler os bytes do **Stream** com os métodos [Read](read-method-ado.md) e [ReadText](readtext-method-ado.md).

  - Gravar quaisquer dados **Stream** que ainda estejam no buffer do ADO para o objeto base com o método [Flush](flush-method-ado.md).

  - Copiar os conteúdos de um **Stream** para outro **Stream** com o método [CopyTo](copyto-method-ado.md).

  - Controlar quantas linhas serão lidas a partir do arquivo fonte com o método [SkipLine](skipline-method-ado.md) e a propriedade [LineSeparator](lineseparator-property-ado.md).

  - Determinar o final da posição do fluxo com a propriedade [EOS](eos-property-ado.md) e o método [SetEOS](seteos-method-ado.md).

  - Salvar e restaurar os arquivos com os métodos [SaveToFile](savetofile-method-ado.md) e [LoadFromFile](loadfromfile-method-ado.md).

  - Especificar o conjunto de caracteres usados para repositório de **Stream** com a propriedade [Charset](charset-property-ado.md).

  - Interromper uma operação **Stream** assíncrona com o método [Cancel](cancel-method-ado.md).

  - Determinar o número de bytes em um **Stream** com a propriedade [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)).

  - Controlar a posição atual dentro de um **Stream** com a propriedade [Position](position-property-ado.md).

  - Determinar o tipo de dados em um **Stream** com a propriedade [Type](type-property-ado-stream.md).

  - Determinar o estado atual do **Stream** (fechado, aberto ou executando) com a propriedade [State](state-property-ado.md).

  - Especificar o modo de acesso para o **Stream** com a propriedade [Mode](mode-property-ado.md).

> [!NOTE]
> [!OBSERVAçãO] As URLs que usam o esquema http chamarão automaticamente o [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obter mais informações, consulte [URLs absolutas e relativas](absolute-and-relative-urls.md).


