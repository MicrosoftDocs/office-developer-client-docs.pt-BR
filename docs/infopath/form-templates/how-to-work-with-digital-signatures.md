---
title: Trabalhar com assinaturas digitais
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- assinaturas digitais [infopath 2007], InfoPath 2007, as assinaturas digitais
localization_priority: Normal
ms.assetid: fd13fb71-aecf-47bb-8a6b-db70bd90ceeb
description: O modelo de objeto do namespace Microsoft.Office.InfoPath fornece recursos para trabalhando de maneira programática com assinaturas digitais.
ms.openlocfilehash: 1277998edf4feb94da40d82372fd4d96fedf2d54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/21/2018
ms.locfileid: "19765661"
---
# <a name="work-with-digital-signatures"></a>Trabalhar com assinaturas digitais

O modelo de objeto do namespace [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) fornece recursos para trabalhando de maneira programática com assinaturas digitais. 
  
## <a name="digital-signature-features"></a>Recursos de assinatura digital

Os recursos de assinaturas digitais fornecidos pelo InfoPath permitem: 
  
- Ativar as assinaturas para o formulário inteiro, ou para conjuntos de dados no formato que pode ser conectado separadamente específicos.
    
- Especifica, para cada conjunto de dados que podem ser assinados, se são permitidas várias assinaturas ou uma única assinatura e quais serão elas se relacionam. Por exemplo, você pode especificar estarem ou assinaturas colegas paralelas ou se cada nova assinatura countersigns todas as assinaturas anteriores.
    
- Especifica uma mensagem a ser mostrada para os usuários do formulário como eles assinem o formulário.
    
- Inserir e ver uma assinatura do documento. 
    
- Modo de exibição não repúdio informações verificáveis que foi adicionadas para cada assinatura para aumentar a segurança. Essas informações adicionais, que inclui um modo de exibição do formulário como ela foi apresentada para cada signatário, é parte da assinatura e não podem ser removidas sem invalidar a assinatura. A qualquer momento, você pode recuperar esses dados clicando na assinatura do formulário para exibir a caixa de diálogo **Verificar Assinatura Digital** . 
    
- Beneficie-se de um modelo de objeto para trabalhar com assinaturas digitais. Adicione informações personalizadas para o bloco de assinatura em formulários totalmente confiáveis através do modelo de objeto de assinatura digital. 
    
## <a name="overview-of-the-digital-signatures-object-model"></a>Visão geral do modelo de objeto de assinaturas digitais

### <a name="the-sign-event"></a>O evento de entrada

O modelo de objeto para assinaturas digitais fornece o evento a seguir.
  
|**Nome**|**Descrição**|
|:-----|:-----|
|[Sinal](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) <br/> |Ocorre depois que um conjunto de dados foi selecionado para fazer logon.  <br/> Você pode usar esse evento para manipular os dados armazenados em assinaturas digitais. Por exemplo, você pode adicionar dados a partir de um servidor de carimbo de hora confiável, ou adicionar uma referenda no servidor da transação. Você também pode usar esse evento para bloquear a assinatura se o usuário atual não for membro de um grupo específico.  <br/> |
   
### <a name="the-signeventargs-object"></a>O objeto SignEventArgs

Um manipulador de eventos para o evento de [entrada](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) pode trabalhar com o objeto de evento [SignEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.aspx) , que fornece as seguintes propriedades. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignedDataBlock.aspx) <br/> |Obtém o conjunto de dados que gerou o evento de [entrada](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) .  <br/> |
|[SignatureWizard](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignatureWizard.aspx) <br/> |Obtém ou define se deseja exibir a caixa de diálogo **Assinaturas digitais** .  <br/> |
   
> [!NOTE]
> No modelo de objeto de código gerenciado [SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) fornecido com o InfoPath 2003, o objeto de evento para o evento [OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2.OnSign.aspx) [SignEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.aspx) fornece uma propriedade **XDocument** para acessar o ** XDocument** objeto do formulário associado ao evento. Isso não é necessário com modelos de formulários criados com o InfoPath Forms Services ou do InfoPath usando o modelo de objeto [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) porque os membros do modelo de objeto da classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) podem ser acessados no código de formulário usando o **isso **(C#) ou a palavra-chave **Me** (Visual Basic). Por exemplo, para acessar a propriedade [entrou](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx) da classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) para determinar se um formulário é assinado, você pode digitar um `this.Signed` ou`Me.Signed.`
  
### <a name="collections-and-objects"></a>Objetos e coleções

O modelo de objeto para assinaturas digitais fornece as seguintes coleções.
  
|**Nome**|**Descrição**|
|:-----|:-----|
|[SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) <br/> |A coleção dos objetos [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) no modelo de formulário, como definido no tempo de design no modo de design do InfoPath.  <br/> A coleção de [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) implementa propriedades que podem ser usadas para acessar os objetos [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) associados a um formulário. O objeto de [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) associado a um formulário é acessível através da propriedade [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx) da classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) .  <br/> |
|[SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) <br/> |Contém uma coleção de objetos [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) para cada objeto [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) no formulário.  <br/> A classe [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) implementa propriedades e um método que pode ser usado para acessar objetos associados a [assinatura](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) de um formulário e criar uma assinatura. O objeto de [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) associado a um [objeto SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) é acessível usando a propriedade [Signatures](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Signatures.aspx) .  <br/> Quando você usa o método [CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) da classe [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) , mantenha em mente que a assinatura não é gravada até o [sinal de](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) método for chamado em objeto [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) . Esses métodos podem ser chamados somente do manipulador de eventos de **entrada** de um modelo de formulário totalmente confiável.  <br/> |
   
O modelo de objeto para assinaturas digitais fornece os seguintes objetos.
  
|**Nome**|**Descrição**|
|:-----|:-----|
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |Representa um conjunto de dados assinados em um formulário. O objeto [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) fornece um número de propriedades e um método que pode ser usado para interagir programaticamente com um conjunto de dados assinados.  <br/> |
|[Assinatura](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |Representa uma assinatura digital que foi adicionada a um formulário ou um conjunto de dados assinados em um formulário. O objeto [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) implementa propriedades que podem ser usadas para recuperar informações sobre a assinatura digital e o método de [entrada](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) para escrever o bloco de assinatura digital XML e seu valor de hash criptográfico de computação.  <br/> |
|[Certificado](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.aspx) <br/> |Representa o certificado digital x. 509 que foi usado para criar a assinatura.  <br/> |
   
## <a name="working-with-digital-signatures-programmatically"></a>Trabalhando de maneira programática com assinaturas digitais

O modelo de objeto do namespace [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) fornece membros para interação com assinaturas digitais programaticamente. Em particular, formulários totalmente confiáveis podem adicionar informações personalizadas para o bloco de assinatura antes que ele seja confirmado, de acordo com a seguinte linha de tempo: 
  
1. Usuário optar por adicionar uma assinatura digital a um formulário.
    
2. A caixa de diálogo **Assinaturas digitais** é exibida, o usuário clicar em **Adicionar**e, em seguida, seleciona os dados para entrar.
    
3. O evento de [entrada](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) para os dados selecionados representados pelo objeto [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) é gerado e o método [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) do objeto [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) e o método de [CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) do [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) coleção são executados. 
    
4. Quaisquer ações personalizadas opcionais são executadas.
    
5. O método [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) do objeto [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) é executado. 
    
6. A caixa de diálogo de **entrada** é exibida para digitar um nome (ou selecionando uma imagem da assinatura), selecionando um certificado para assinar com e insira comentários. 
    
7. Quando o botão de **entrada** é clicado, a assinatura é adicionada à coleção de assinaturas para o formulário e as informações de não-recusa são capturadas e salvo com a assinatura (que pode ser exibida mais tarde clicando em **Exibir formulário assinado** sobre o ** Assinaturas digitais** caixa de diálogo e clicando em **ver as informações de assinatura adicionais que foram coletadas**).
    
O exemplo a seguir chama o método [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) quando o usuário entra os dados selecionados e countersigns a assinatura com um valor de carimbo de hora recuperado de um serviço de carimbo de hora confiável. 
  
```cs
public void FormEvents_Sign(object sender, SignEventArgs e)
{
   // Add a new Signature object to the SignedDataBlockCollection.
   Signature thisSignature = 
      e.SignedDataBlock.Signatures.CreateSignature();
   // Write the XML digital signature block and compute hash
   // for signed data.
   thisSignature.Sign();
   // Countersign the signature with a trusted timestamp.
   // Get the XML node storing the signature block.
   XPathNavigator oNodeSig = thisSignature.SignatureBlockXmlNode;
   XPathNavigator oNodeSigValue = 
      oNodeSig.SelectSingleNode(
      ".//*[local-name(.)='signatureValue']");
   // Get timestamp from a trusted timestamp service (fictitious).
   MyTrustedTimeStampService s = new MyTrustedTimeStampService();
   string strVerifiedTimeStamp = s.AddTimeStamp(oNodeSigValue.Value);
   // Add the value returned from the timestamp service to the 
   // unsigned part of the signature block.
   XPathNavigator oNodeObj = 
      oNodeSig.SelectSingleNode(".//*[local-name(.)='Object']");
   XPathNavigator oNode = oNodeObj.Clone();
   oNode.SetValue(strVerifiedTimeStamp);
   oNodeObj.MoveToParent();
   oNodeObj.AppendChild(oNode);
   e.SignatureWizard = false;
}
```

```vb
Public Sub FormEvents_Sign(ByVal sender As Object, _
   ByVal e As SignEventArgs)
   ' Add a new Signature object to the SignedDataBlockCollection.
   Dim thisSignature As Signature = 
      e.SignedDataBlock.Signatures.CreateSignature
   ' Write the XML digital signature block and compute hash
   ' for signed data.
   thisSignature.Sign()
   ' Countersign the signature with a trusted timestamp.
   ' Get the XML node storing the signature block
   Dim oNodeSig As XPathNavigator  = _
      thisSignature.SignatureBlockXmlNode
   Dim oNodeSigValue As XPathNavigator  = _
      oNodeSig.SelectSingleNode(_
      ".//*[local-name(.)='signatureValue']")
   ' Get timestamp from a trusted timestamp service (fictitious).
   Dim s As MyTrustedTimeStampService = New MyTrustedTimeStampService()
   Dim strVerifiedTimeStamp As String  = _
      s.AddTimeStamp(oNodeSigValue.Value)
   ' Add the value returned from the timestamp service to the 
   ' unsigned part of the signature block.
   Dim oNodeObj As XPathNavigator  = 
      oNodeSig.SelectSingleNode(".//*[local-name(.)='Object']")
   Dim oNode As XPathNavigator  = oNodeObj.Clone()
   oNode.SetValue(strVerifiedTimeStamp)
   oNodeObj.MoveToParent()
   oNodeObj.AppendChild(oNode)
   e.SignatureWizard = False
```


