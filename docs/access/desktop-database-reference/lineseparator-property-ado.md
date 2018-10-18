---
<<<<<<< Título cabeça: propriedade LineSeparator (ADO) TOCTitle: propriedade LineSeparator (ADO) === título: propriedade LineSeparator (ADO) TOCTitle: propriedade LineSeparator (ADO)
>>>>>>> ms:assetid de mestre: 9f1323cd-d4ed-2bfa-554b-faebab529548 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15) ms:contentKeyID: ms.date 48546676: 18/09/2015 mtps_version: v=office.15
---

<<<<<<< Cabeça
# <a name="lineseparator-property-ado"></a>Propriedade LineSeparator (ADO)
=======
# <a name="lineseparator-property-ado"></a>Propriedade LineSeparator (ADO)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013

Indica o caractere binário a ser usado como o separador de linha nos objetos [Stream](stream-object-ado.md) de texto.

<<<<<<< Cabeça
## <a name="settings-and-return-values"></a>Configurações e valor de retorno
=======
## <a name="settings-and-return-values"></a>Configurações e valores de retorno
>>>>>>> mestre

Define ou retorna um valor [LineSeparatorsEnum](lineseparatorsenum.md) que indica o caractere do separador de linha usado no **Stream**. O valor padrão é **adCRLF**.

## <a name="remarks"></a>Comentários

**LineSeparator** é usada para interpretar as linhas ao ler o conteúdo de um **Stream** de texto. As linhas podem ser ignoradas com o método [SkipLine](skipline-method-ado.md).

**LineSeparator** é usada apenas com objetos **Stream** de texto ([Type](type-property-ado-stream.md) é **adTypeText**). Esta propriedade será ignorada se **Type** for **adTypeBinary**.

