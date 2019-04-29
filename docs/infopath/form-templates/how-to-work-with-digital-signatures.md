---
title: Trabalhar com assinaturas digitais
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- assinaturas digitais [InfoPath 2007], InfoPath 2007, assinaturas digitais
localization_priority: Normal
ms.assetid: fd13fb71-aecf-47bb-8a6b-db70bd90ceeb
description: O modelo de objeto do namespace Microsoft. Office. InfoPath fornece recursos para trabalhar com assinaturas digitais programaticamente.
ms.openlocfilehash: ea657f80f6e38a06a91e19c245eadc203c7c580c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425572"
---
# <a name="work-with-digital-signatures"></a>Trabalhar com assinaturas digitais

O modelo de objeto do namespace [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) fornece recursos para trabalhar com assinaturas digitais programaticamente. 
  
## <a name="digital-signature-features"></a>Recursos de assinatura digital

Os recursos de assinaturas digitais fornecidos pelo InfoPath permitem: 
  
- Habilitar assinaturas para o formulário inteiro ou para conjuntos específicos de dados no formulário que podem ser assinados separadamente.
    
- Especifique, para cada conjunto de dados que podem ser assinados, se uma assinatura única ou várias assinaturas são permitidas e qual será a relação. Por exemplo, você pode especificar se são assinaturas paralelas ou se cada nova assinatura assina todas as assinaturas anteriores.
    
- Especifique uma mensagem a ser mostrada para os usuários de forma que eles assinem o formulário.
    
- Insira e veja uma assinatura no documento. 
    
- Exibir informações verificáveis de não repúdio que foram adicionadas a cada assinatura para aumentar a segurança. Essas informações adicionais, que incluem um modo de exibição do formulário como foram apresentadas a cada signatário, fazem parte da assinatura e não podem ser removidas sem invalidar a assinatura. A qualquer momento, você pode recuperar esses dados clicando na assinatura no formulário para exibir a caixa de diálogo **verificar assinatura digital** . 
    
- Aproveite um modelo de objeto para trabalhar com assinaturas digitais. Adicione informações personalizadas ao bloco de assinatura em formulários totalmente confiáveis por meio do modelo de objeto de assinatura digital. 
    
## <a name="overview-of-the-digital-signatures-object-model"></a>Visão geral do modelo de objeto de assinaturas digitais

### <a name="the-sign-event"></a>O evento Sign

O modelo de objeto para assinaturas digitais fornece o seguinte evento.
  
|**Nome**|**Descrição**|
|:-----|:-----|
|[Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) <br/> |Ocorre depois que um conjunto de dados é selecionado para assinar.  <br/> Você pode usar esse evento para manipular os dados armazenados na assinatura digital. Por exemplo, você pode adicionar dados de um servidor de carimbo de data/hora confiável ou adicionar uma referenda do lado do servidor da transação. Você também pode usar esse evento para bloquear a assinatura se o usuário atual não for um membro de um grupo específico.  <br/> |
   
### <a name="the-signeventargs-object"></a>O objeto Signeventargs

Um manipulador de eventos para o evento [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) pode funcionar com o objeto Event de [signeventargs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.aspx) , que fornece as propriedades a seguir. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignedDataBlock.aspx) <br/> |Obtém o conjunto de dados que gerou o evento [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) .  <br/> |
|[SignatureWizard](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignatureWizard.aspx) <br/> |Obtém ou define se a caixa de diálogo **assinaturas digitais** deve ser exibida.  <br/> |
   
> [!NOTE]
> No modelo de objeto de código gerenciado [Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) que acompanha o InfoPath 2003, o objeto de evento [SignEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.aspx) para o evento OnSign fornece uma propriedade [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2.OnSign.aspx) **XDocument** para acessar o ** Objeto XDocument** do formulário associado ao evento. Isso não é necessário com modelos de formulário criados com o InfoPath Forms Services ou o InfoPath usando o modelo de objeto [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) porque os membros de modelo de objeto da classe XmlForm podem ser acessados em código de formulário usando [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) **este **(C#) ou **me** (Visual Basic) palavra-chave. Por exemplo, para acessar a propriedade [signed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx) da classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) para determinar se um formulário está assinado, você pode digitar um `this.Signed` ou`Me.Signed.`
  
### <a name="collections-and-objects"></a>Coleções e objetos

O modelo de objeto para assinaturas digitais fornece as seguintes coleções.
  
|**Nome**|**Descrição**|
|:-----|:-----|
|[SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) <br/> |A coleção dos objetos [signedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) no modelo de formulário, conforme definido no tempo de design no modo de design do InfoPath.  <br/> A coleção [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) implementa propriedades que podem ser usadas para acessar os objetos [signedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) associados a um formulário. O objeto [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) associado a um formulário pode ser acessado através da propriedade [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx) da classe XmlForm. [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx)  <br/> |
|[Signaturecollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) <br/> |Contém uma coleção de objetos [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) para cada objeto [signedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) no formulário.  <br/> A [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) classe signaturecollection implementa propriedades e um método que pode ser usado para acessar os objetos de [assinatura](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) associados de um formulário e para criar uma assinatura. O [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) objeto signaturecollection associado a um [signedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) pode ser acessado usando a propriedade [Signatures](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Signatures.aspx) .  <br/> Quando você usa o [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) método CreateSignature da classe [signaturecollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) , tenha em mente que a assinatura não é gravada até que o método [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) seja chamado no objeto [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) . Esses métodos podem ser chamados apenas do manipulador de eventos **assinar** de um modelo de formulário totalmente confiável.  <br/> |
   
O modelo de objeto para assinaturas digitais fornece os seguintes objetos.
  
|**Nome**|**Descrição**|
|:-----|:-----|
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |Representa um conjunto de dados assináveis em um formulário. O objeto [signedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) fornece várias propriedades e um método que pode ser usado para interagir programaticamente com um conjunto de dados assináveis.  <br/> |
|[Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |Representa uma assinatura digital que foi adicionada a um formulário ou a um conjunto de dados assináveis em um formulário. O objeto [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) implementa as propriedades que podem ser usadas para recuperar informações sobre a assinatura digital e o método [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) para gravar o bloco de assinatura digital XML e a computação de seu valor de hash criptográfico.  <br/> |
|[Certificate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.aspx) <br/> |Representa o certificado digital X. 509 que foi usado para criar a assinatura.  <br/> |
   
## <a name="working-with-digital-signatures-programmatically"></a>Trabalhar com assinaturas digitais de forma programática

O modelo de objeto do namespace [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) fornece membros para interagir com assinaturas digitais programaticamente. Em particular, os formulários totalmente confiáveis podem adicionar informações personalizadas ao bloco de assinatura antes de serem confirmadas, de acordo com a seguinte linha do tempo: 
  
1. O usuário opta por adicionar uma assinatura digital a um formulário.
    
2. A caixa de diálogo **assinaturas digitais** é exibida, o usuário clica em **Adicionar**e, em seguida, seleciona os dados a serem assinados.
    
3. O evento [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) dos dados selecionados, representado pelo objeto [signedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) , é gerado e o método [Sign ()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) do objeto [signedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) e o método [CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) de signaturecollection [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) coleção são executadas. 
    
4. Qualquer ação personalizada opcional é executada.
    
5. O método [Sign ()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) do objeto [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) é executado. 
    
6. A caixa de diálogo **assinar** é exibida para digitar um nome (ou selecionar uma imagem de assinatura), selecionar um certificado para entrar e inserir comentários. 
    
7. Quando o botão de **sinal** é clicado, a assinatura é adicionada à coleção de assinaturas para o formulário e as informações de não recusa são capturadas e salvas com a assinatura (que pode ser exibida posteriormente clicando em **Exibir formulário assinado** no ** Assinaturas digitais** e, em seguida, clique em **ver as informações adicionais de assinatura coletadas**.
    
O exemplo a seguir invoca o método [Sign ()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) quando o usuário assina os dados selecionados e o referenda com um valor de carimbo de data/hora recuperado de um serviço de carimbo de data/hora confiável. 
  
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


