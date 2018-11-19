---
title: Método Open (Stream do ADO)
TOCTitle: Open method (ADO Stream)
ms:assetid: fa2e6aaa-e9f5-009c-f3a0-050a00abf9b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250275(v=office.15)
ms:contentKeyID: 48548833
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b20a68f1707e496b92ba8acbf8bc7ed8d8a2b058
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026411"
---
# <a name="open-method-ado-stream"></a>Método Open (Stream do ADO)


**Aplica-se a**: Access 2013, o Office 2013


Abre um objeto [Stream](stream-object-ado.md) para manipular fluxos de dados de texto ou binários.

## <a name="syntax"></a>Sintaxe

*Stream*. Abra o *código-fonte*, *modo*, *OpenOptions*, *nome de usuário*, *senha*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Source* |Opcional. Um valor **Variant** que especifica a fonte dos dados para o **Stream**. *Fonte* pode conter uma sequência de URL absoluta que aponta para um nó existente em uma estrutura de árvore conhecida, como um sistema de email ou o arquivo. Uma URL deve ser especificada usando a palavra-chave URL ("URL =*esquema*://*server*/*pasta*"). Como alternativa, a *fonte* pode conter uma referência a um objeto [Record](record-object-ado.md) já aberto, que abre um fluxo padrão associado ao **registro**. Se a *fonte* não for especificado, um **fluxo** é instanciado e aberto, associados a nenhuma fonte subjacente por padrão. Para obter mais informações sobre esquemas URL e seus provedores associados, consulte [URLs absolutas e relativas](absolute-and-relative-urls.md).|
|*Mode* |Opcional. Um valor [ConnectModeEnum](connectmodeenum.md) que especifica o modo de acesso para o **Stream** resultante (por exemplo, leitura/gravação ou somente leitura). O valor padrão é **adModeUnknown**. Consulte a propriedade [Mode](mode-property-ado.md) para obter mais informações sobre modos de acesso. Se o *modo* não for especificado, ele é herdado pelo objeto de origem. Por exemplo, se o **Record** de origem for aberto no modo somente leitura, o **Stream** também será aberto no modo somente leitura por padrão.|
|*OpenOptions* |Opcional. Um valor [StreamOpenOptionsEnum](streamopenoptionsenum.md). O valor padrão é **adOpenStreamUnspecified**.|
|*UserName* |Opcional. Um valor **String** que contém a identificação do usuário que, se necessária, acessa o objeto **Stream**.|
|*Password* |Opcional. Um valor **String** que contém a senha que, se necessária, acessa o objeto **Stream**.|

## <a name="remarks"></a>Comentários

Quando um objeto **Record** é passado como o parâmetro source, a *ID de usuário* e os parâmetros de *senha* não são usados como acesso ao objeto **registro** já está disponível. Da mesma forma, o [modo](mode-property-ado.md) do objeto **Record** é transferida para o objeto **Stream** . Quando o *código-fonte* não for especificado, o **fluxo** aberto não contém dados e tem um [tamanho](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) zero (0). Para evitar a perda de todos os dados que são gravados este **fluxo** quando o **fluxo** é fechado, salve o **Stream** com os métodos [CopyTo](copyto-method-ado.md) ou [SaveToFile](savetofile-method-ado.md) ou salvá-lo para outro local de memória.

Um valor de *OpenOptions* de **adOpenStreamFromRecord** identifica o conteúdo do parâmetro *fonte* a ser um objeto de **registro** já aberto. O comportamento padrão é tratar a *fonte* como uma URL que aponta diretamente para um nó em uma estrutura de árvore, como um arquivo. O fluxo padrão associado a esse nó será aberto.

Enquanto o **Stream** não estiver aberto, será possível ler todas as propriedades somente leitura do **Stream**. Se um **Stream** for aberto assincronamente, todas as operações subsequentes (que não sejam a verificação de [State](state-property-ado.md) e outras propriedades somente leitura) serão bloqueadas até que a operação **Open** seja concluída.

Além das opções discutidas acima, por meio da não especificação de *Source* é possível simplesmente instanciar um objeto **Stream** em memória sem associá-lo a uma fonte base. Você pode adicionar dados dinamicamente ao fluxo simplesmente pela gravação de dados de texto ou binários no **Stream** com [Write](write-method-ado.md) ou [WriteText](writetext-method-ado.md), ou pelo carregamento de dados a partir de um arquivo com [LoadFromFile](loadfromfile-method-ado.md).

