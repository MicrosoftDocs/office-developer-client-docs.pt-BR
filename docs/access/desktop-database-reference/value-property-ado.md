---
<<<<<<< Título cabeça: valor Property (ADO) TOCTitle: valor de propriedade (ADO) === título: valor de propriedade (ADO) TOCTitle: valor de propriedade (ADO)
>>>>>>> ms:assetid de mestre: ff21d122-98e3-2b48-d92f-e696b8079fc5 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250310(v=office.15) ms:contentKeyID: ms.date 48548958: 18/09/2015 mtps_version: v=office.15
---

<<<<<<< Cabeça
# <a name="value-property-ado"></a>Propriedade Value (ADO)
=======
# <a name="value-property-ado"></a>Propriedade Value (ADO)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013

Indica o valor atribuído a um objeto [Field](field-object-ado.md), [Parameter](parameter-object-ado.md) ou [Property](property-object-ado.md).

<<<<<<< Cabeça
## <a name="settings-and-return-values"></a>Configurações e valor de retorno
=======
## <a name="settings-and-return-values"></a>Configurações e valores de retorno
>>>>>>> mestre

Define ou retorna um valor **Variant** que indica o valor do objeto. O valor padrão depende da propriedade [Type](type-property-ado.md).

## <a name="remarks"></a>Comentários

Utilize a propriedade **Value** para definir ou retornar dados a partir dos objetos **Field**, para definir ou retornar valores de parâmetro com os objetos **Parameter**, ou para definir ou retornar definições de propriedade com os objetos **Property**. A definição da propriedade **Value** como leitura/gravação ou somente leitura depende de diversos fatores  consulte os tópicos do respectivo objeto para obter mais informações.

O ADO permite a definição e o retorno de dados binários longos com a propriedade **Value**.


> [!NOTE]
> <P>[!OBSERVAçãO] Para os objetos <STRONG>Parameter</STRONG>, o ADO lê a propriedade <STRONG>Value</STRONG> somente uma vez a partir do provedor. Se um comando contiver um <STRONG>Parameter</STRONG> cuja propriedade <STRONG>Value</STRONG> esteja vazia e você criar um <A href="recordset-object-ado.md">Recordset</A> a partir do comando, certifique-se de fechar o <STRONG>Recordset</STRONG> antes de recuperar a propriedade <STRONG>Value</STRONG>. Caso contrário, para alguns provedores, a propriedade <STRONG>Value</STRONG> poderá ficar vazia e não conterá o valor correto.</P>



Para novos objetos **Field** que foram acrescentados à coleção [Fields](fields-collection-ado.md) de um objeto [Record](record-object-ado.md), a propriedade **Value** deverá ser definida antes que qualquer outra propriedade **Field** seja especificada. Primeiro, um valor específico para a propriedade **Value** deve ser atribuído e o método [Update](update-method-ado.md) deve ser chamado na coleção **Fields**. Assim, outras propriedades, como [Type](type-property-ado.md) ou [Attributes](attributes-property-ado.md), poderão ser acessadas.

