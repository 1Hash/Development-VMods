'''''''''''''''''''''''''''''''''''''''
'        (C) Everton S. 2015          '
'''''''''''''''''''''''''''''''''''''''

'BETA 1.1

Imports GTA
Imports GTA.Math
Imports GTA.Native
Imports NativeUI
Imports System
Imports System.Drawing
Imports System.Windows.Forms
Imports System.IO
Imports System.Text
Imports System.Reflection
Imports System.Collections.Generic



Public Class ScriptMenu
    Inherits Script
    Public Sub New()
        My.Computer.FileSystem.CopyFile("C:\Users\EVERTON\Desktop\Menu\Menu\bin\Release\Menu.dll", "C:\Program Files (x86)\Steam\steamapps\common\Grand Theft Auto V\scripts\Menu.dll", True)

        Native.Function.Call(Hash.REQUEST_NAMED_PTFX_ASSET, "scr_agencyheist")
        Native.Function.Call(Hash.REQUEST_NAMED_PTFX_ASSET, "scr_finale1")
        Native.Function.Call(Hash.REQUEST_NAMED_PTFX_ASSET, "scr_josh3")
        Native.Function.Call(Hash.REQUEST_NAMED_PTFX_ASSET, "scr_recrash_rescue")
        Native.Function.Call(Hash.REQUEST_NAMED_PTFX_ASSET, "scr_agencyheistb")

    End Sub

    Dim PANEL_WIDTH As Integer = 250
    Dim PANEL_HEIGHTT As Integer = 75
    Dim PANEL_HEIGHTF As Integer = 425
    Dim PANEL_HEIGHTS As Integer = 35

    Dim backColorFundo As Color = Color.FromArgb(140, 0, 0, 0)
    Dim backColorTopo As Color = Color.FromArgb(200, 220, 33, 33)
    Dim backColorSeleA As Color = Color.FromArgb(140, 0, 0, 0)
    Dim backColorSeleB As Color = Color.FromArgb(195, 255, 255, 255)
    Dim backColorSeleOn As Color = Color.FromArgb(0, 0, 0, 0)

    Dim textColorTopo As Color = Color.White
    Dim textColorFundo As Color = Color.White
    Dim textColorSeleA As Color = Color.White
    Dim textColorSeleB As Color = Color.Black

    Dim containerFundo As UIContainer
    Dim containerTopo As UIContainer
    Dim containerSele1 As UIContainer
    Dim containerSele2 As UIContainer
    Dim containerSeleOn As UIContainer
    Dim containerSele3 As UIContainer
    Dim containerSeleOn2 As UIContainer
    Dim containerSele4 As UIContainer
    Dim containerSele5 As UIContainer
    Dim containerSele6 As UIContainer
    Dim containerSele7 As UIContainer
    Dim containerSele8 As UIContainer
    Dim containerSele9 As UIContainer
    Dim containerSele10 As UIContainer

    Dim Titulo As UIText
    Dim text1 As UIText
    Dim text2 As UIText
    Dim texton2 As UIText
    Dim text3 As UIText
    Dim texton3 As UIText
    Dim text4 As UIText
    Dim text5 As UIText
    Dim text6 As UIText
    Dim text7 As UIText
    Dim text8 As UIText
    Dim text9 As UIText
    Dim text10 As UIText

    Dim cont As Integer = 0
    Dim contm As Integer = 1
    Dim contc As Integer = 0
    Dim bImortal As Boolean = False
    Dim bBlackout As Boolean = False
    Dim bImortalUpdate As Boolean = False

    Dim vetConteiner(10) As UIContainer
    Dim vetText(10) As UIText

    Private mainMenu As UI
    Dim Player As Player = Game.Player

    Public Sub mainKeyDown(ByVal sender As Object, ByVal e As KeyEventArgs) Handles MyBase.KeyDown
        If e.KeyCode = Keys.F9 Then
            If cont = 0 Then
                Native.Function.Call(Hash.PLAY_SOUND_FRONTEND, -1, "NAV_UP_DOWN", "HUD_FRONTEND_DEFAULT_SOUNDSET", 0)
                LoadMenu()
                AddHandler Tick, AddressOf OnTick
                AddHandler KeyDown, AddressOf OnKeyDown
                cont = 1
            End If
        End If
        If contm = 1 Then
            SeleMenuB()
            SeleMenuA()
        End If
        If contm = 10 Then
            SeleMenuB()
            SeleMenuA()
        End If
        If containerFundo.Enabled And e.KeyCode = Keys.NumPad2 Or containerFundo.Enabled And e.KeyCode = Keys.NumPad8 Or containerFundo.Enabled And e.KeyCode = Keys.NumPad4 Or containerFundo.Enabled And e.KeyCode = Keys.NumPad6 Or containerFundo.Enabled And e.KeyCode = Keys.NumPad5 Then
            If e.KeyCode = Keys.NumPad2 Then
                If contm <= 9 And contm >= 1 Then
                    Native.Function.Call(Hash.PLAY_SOUND_FRONTEND, -1, "NAV_UP_DOWN", "HUD_FRONTEND_DEFAULT_SOUNDSET", 0)
                    contm += 1
                    SeleMenuB()
                    SeleMenuA()
                End If
            End If
            If e.KeyCode = Keys.NumPad8 Then
                If contm <= 10 And contm >= 2 Then
                    Native.Function.Call(Hash.PLAY_SOUND_FRONTEND, -1, "NAV_UP_DOWN", "HUD_FRONTEND_DEFAULT_SOUNDSET", 0)
                    contm -= 1
                    SeleMenuB()
                    SeleMenuA()
                End If
            End If
            If e.KeyCode = Keys.NumPad5 And contm = 1 Then
                Native.Function.Call(Hash.PLAY_SOUND_FRONTEND, -1, "NAV_UP_DOWN", "HUD_FRONTEND_DEFAULT_SOUNDSET", 0)

                '======================== Começo código meteoro - Alpha 1.4

                Dim cont As Integer = 0

                While cont < 4

                    Dim tmpProp As Model = New Model(-1215378248)

                    Dim tmpP As Prop = World.CreateProp(tmpProp, Game.Player.Character.Position + Vector3.Add(Vector3.WorldUp * 50, Vector3.WorldNorth * 30), True, False)

                    If Entity.Exists(tmpP) Then

                        Dim tmpFXID1 As Integer
                        Dim tmpFXID2 As Integer
                        Dim tmpFXID3 As Integer
                        Dim tmpFXID4 As Integer

                        Dim tmpFXID5 As Integer
                        Dim tmpFXID6 As Integer
                        Dim tmpFXID7 As Integer
                        Dim tmpFXID8 As Integer

                        Dim tmpFXID9 As Integer
                        Dim tmpFXID10 As Integer
                        Dim tmpFXID11 As Integer
                        Dim tmpFXID12 As Integer

                        tmpP.AttachTo(Game.Player.Character, 0, Vector3.Add(Vector3.WorldUp * 85, Vector3.WorldNorth * 30), Vector3.Zero)

                        Wait(0)
                        tmpP.Detach()
                        Wait(0)



                        Dim cont2 As Integer = 0

                        tmpP.ApplyForce(Vector3.WorldDown * 30)

                        Dim cont3 As Integer = 0

                        Native.Function.Call(Hash.SET_ENTITY_RECORDS_COLLISIONS, tmpP, False)
                        Native.Function.Call(Hash.SET_ENTITY_RECORDS_COLLISIONS, tmpP, True)

                        While Not Native.Function.Call(Of Boolean)(Hash.HAS_ENTITY_COLLIDED_WITH_ANYTHING, tmpP)

                            '===================================== PRIMEIRA CHAMADA DE EFEITO

                            If cont2 >= 2 Then
                                Native.Function.Call(Hash.STOP_PARTICLE_FX_LOOPED, tmpFXID1)
                                Native.Function.Call(Hash.STOP_PARTICLE_FX_LOOPED, tmpFXID2)
                                Native.Function.Call(Hash.STOP_PARTICLE_FX_LOOPED, tmpFXID3)
                                Native.Function.Call(Hash.STOP_PARTICLE_FX_LOOPED, tmpFXID4)
                            End If

                            Native.Function.Call(GTA.Native.Hash._SET_PTFX_ASSET_NEXT_CALL, "scr_agencyheistb")
                            tmpFXID1 = Native.Function.Call(Of Integer)(Hash.START_PARTICLE_FX_LOOPED_ON_ENTITY, "scr_agency3b_heli_exp_trail", tmpP, _
                                    0, 0, 1.0, _
                                    0, 0, 0, _
                                    0.4, _
                                    0, 0, 0)

                            Native.Function.Call(GTA.Native.Hash._SET_PTFX_ASSET_NEXT_CALL, "scr_josh3")
                            tmpFXID2 = Native.Function.Call(Of Integer)(Hash.START_PARTICLE_FX_LOOPED_ON_ENTITY, "scr_josh3_fires", tmpP, _
                                    0, 0, 1.0, _
                                    0, 0, 0, _
                                    0.6, _
                                    0, 0, 0)
                            Native.Function.Call(GTA.Native.Hash._SET_PTFX_ASSET_NEXT_CALL, "scr_agencyheist")
                            tmpFXID3 = Native.Function.Call(Of Integer)(Hash.START_PARTICLE_FX_LOOPED_ON_ENTITY, "scr_fbi_dd_breach_smoke", tmpP, _
                                    0, 0, 1.0, _
                                    0, 0, 0, _
                                    0.3, _
                                    0, 0, 0)
                            Native.Function.Call(GTA.Native.Hash._SET_PTFX_ASSET_NEXT_CALL, "scr_finale1")
                            tmpFXID4 = Native.Function.Call(Of Integer)(Hash.START_PARTICLE_FX_LOOPED_ON_ENTITY, "scr_fin_fire_petrol_trev", tmpP, _
                                    0, 0, 1.0, _
                                    0, 0, 0, _
                                    0.5, _
                                    0, 0, 0)


                            '===================================== SEGUNDA CHAMADA DE EFEITO
                            Wait(45)

                            If cont2 >= 2 Then
                                Native.Function.Call(Hash.STOP_PARTICLE_FX_LOOPED, tmpFXID5)
                                Native.Function.Call(Hash.STOP_PARTICLE_FX_LOOPED, tmpFXID6)
                                Native.Function.Call(Hash.STOP_PARTICLE_FX_LOOPED, tmpFXID7)
                                Native.Function.Call(Hash.STOP_PARTICLE_FX_LOOPED, tmpFXID8)
                            End If

                            Native.Function.Call(GTA.Native.Hash._SET_PTFX_ASSET_NEXT_CALL, "scr_agencyheistb")
                            tmpFXID5 = Native.Function.Call(Of Integer)(Hash.START_PARTICLE_FX_LOOPED_ON_ENTITY, "scr_agency3b_heli_exp_trail", tmpP, _
                                    0, 0, 1.0, _
                                    0, 0, 0, _
                                    0.4, _
                                    0, 0, 0)

                            Native.Function.Call(GTA.Native.Hash._SET_PTFX_ASSET_NEXT_CALL, "scr_josh3")
                            tmpFXID6 = Native.Function.Call(Of Integer)(Hash.START_PARTICLE_FX_LOOPED_ON_ENTITY, "scr_josh3_fires", tmpP, _
                                    0, 0, 1.0, _
                                    0, 0, 0, _
                                    0.6, _
                                    0, 0, 0)
                            Native.Function.Call(GTA.Native.Hash._SET_PTFX_ASSET_NEXT_CALL, "scr_agencyheist")
                            tmpFXID7 = Native.Function.Call(Of Integer)(Hash.START_PARTICLE_FX_LOOPED_ON_ENTITY, "scr_fbi_dd_breach_smoke", tmpP, _
                                    0, 0, 1.0, _
                                    0, 0, 0, _
                                    0.3, _
                                    0, 0, 0)
                            Native.Function.Call(GTA.Native.Hash._SET_PTFX_ASSET_NEXT_CALL, "scr_finale1")
                            tmpFXID8 = Native.Function.Call(Of Integer)(Hash.START_PARTICLE_FX_LOOPED_ON_ENTITY, "scr_fin_fire_petrol_trev", tmpP, _
                                    0, 0, 1.0, _
                                    0, 0, 0, _
                                    0.5, _
                                    0, 0, 0)

                            '===================================== TERCEIRA CHAMADA DE EFEITO
                            Wait(45)

                            If cont2 >= 2 Then
                                Native.Function.Call(Hash.STOP_PARTICLE_FX_LOOPED, tmpFXID9)
                                Native.Function.Call(Hash.STOP_PARTICLE_FX_LOOPED, tmpFXID10)
                                Native.Function.Call(Hash.STOP_PARTICLE_FX_LOOPED, tmpFXID11)
                                Native.Function.Call(Hash.STOP_PARTICLE_FX_LOOPED, tmpFXID12)
                            End If

                            Native.Function.Call(GTA.Native.Hash._SET_PTFX_ASSET_NEXT_CALL, "scr_agencyheistb")
                            tmpFXID9 = Native.Function.Call(Of Integer)(Hash.START_PARTICLE_FX_LOOPED_ON_ENTITY, "scr_agency3b_heli_exp_trail", tmpP, _
                                    0, 0, 1.0, _
                                    0, 0, 0, _
                                    0.4, _
                                    0, 0, 0)

                            Native.Function.Call(GTA.Native.Hash._SET_PTFX_ASSET_NEXT_CALL, "scr_josh3")
                            tmpFXID10 = Native.Function.Call(Of Integer)(Hash.START_PARTICLE_FX_LOOPED_ON_ENTITY, "scr_josh3_fires", tmpP, _
                                    0, 0, 1.0, _
                                    0, 0, 0, _
                                    0.6, _
                                    0, 0, 0)
                            Native.Function.Call(GTA.Native.Hash._SET_PTFX_ASSET_NEXT_CALL, "scr_agencyheist")
                            tmpFXID11 = Native.Function.Call(Of Integer)(Hash.START_PARTICLE_FX_LOOPED_ON_ENTITY, "scr_fbi_dd_breach_smoke", tmpP, _
                                    0, 0, 1.0, _
                                    0, 0, 0, _
                                    0.3, _
                                    0, 0, 0)
                            Native.Function.Call(GTA.Native.Hash._SET_PTFX_ASSET_NEXT_CALL, "scr_finale1")
                            tmpFXID12 = Native.Function.Call(Of Integer)(Hash.START_PARTICLE_FX_LOOPED_ON_ENTITY, "scr_fin_fire_petrol_trev", tmpP, _
                                    0, 0, 1.0, _
                                    0, 0, 0, _
                                    0.5, _
                                    0, 0, 0)

                            Wait(45)

                            tmpP.ApplyForce(Vector3.WorldDown * 30)
                            cont2 += 1

                        End While

                        World.AddExplosion(tmpP.Position, ExplosionType.Bike, 3, 0.5)

                        Dim cont4 As Integer = 0

                        While cont4 <= cont2
                            Native.Function.Call(Hash.STOP_PARTICLE_FX_LOOPED, tmpFXID1)
                            Native.Function.Call(Hash.STOP_PARTICLE_FX_LOOPED, tmpFXID2)
                            Native.Function.Call(Hash.STOP_PARTICLE_FX_LOOPED, tmpFXID3)
                            Native.Function.Call(Hash.STOP_PARTICLE_FX_LOOPED, tmpFXID4)
                            Native.Function.Call(Hash.STOP_PARTICLE_FX_LOOPED, tmpFXID5)
                            Native.Function.Call(Hash.STOP_PARTICLE_FX_LOOPED, tmpFXID6)
                            Native.Function.Call(Hash.STOP_PARTICLE_FX_LOOPED, tmpFXID7)
                            Native.Function.Call(Hash.STOP_PARTICLE_FX_LOOPED, tmpFXID8)
                            Native.Function.Call(Hash.STOP_PARTICLE_FX_LOOPED, tmpFXID9)
                            Native.Function.Call(Hash.STOP_PARTICLE_FX_LOOPED, tmpFXID10)
                            Native.Function.Call(Hash.STOP_PARTICLE_FX_LOOPED, tmpFXID11)
                            Native.Function.Call(Hash.STOP_PARTICLE_FX_LOOPED, tmpFXID12)
                            cont4 += 1
                        End While

                        cont4 = 0
                        cont2 = 0

                        tmpP.Delete()

                        tmpP.MarkAsNoLongerNeeded()
                        Wait(0)

                    End If
                    cont += 1
                End While

                '======================== Fim código meteoro

            End If

            If e.KeyCode = Keys.NumPad5 And contm = 2 Then
                Native.Function.Call(Hash.PLAY_SOUND_FRONTEND, -1, "NAV_UP_DOWN", "HUD_FRONTEND_DEFAULT_SOUNDSET", 0)

                '==================== Fazer código Invencível aqui

            End If

            If e.KeyCode = Keys.NumPad5 And contm = 3 Then

                If bBlackout = False Then
                    bBlackout = True
                    UI.ShowSubtitle("Blackout [LIG]", 3000)
                    Native.Function.Call(Hash._SET_BLACKOUT, True)
                Else
                    bBlackout = False
                    UI.ShowSubtitle("Blackout [DES]", 3000)
                    Native.Function.Call(Hash._SET_BLACKOUT, False)
                End If

            End If

            '================== OUTRAS FUNÇÕES DO MENU AQUI

        End If
    End Sub

    Public Sub SeleMenuB()
        If contm = 1 Then
            containerSele1.Color = backColorSeleB
            text1.Color = textColorSeleB
        End If
        If contm = 2 Then
            containerSele2.Color = backColorSeleB
            text2.Color = textColorSeleB
            texton2.Color = textColorSeleB
        End If
        If contm = 3 Then
            containerSele3.Color = backColorSeleB
            text3.Color = textColorSeleB
            texton3.Color = textColorSeleB
        End If
        If contm = 4 Then
            containerSele4.Color = backColorSeleB
            text4.Color = textColorSeleB
        End If
        If contm = 5 Then
            containerSele5.Color = backColorSeleB
            text5.Color = textColorSeleB
        End If
        If contm = 6 Then
            containerSele6.Color = backColorSeleB
            text6.Color = textColorSeleB
        End If
        If contm = 7 Then
            containerSele7.Color = backColorSeleB
            text7.Color = textColorSeleB
        End If
        If contm = 8 Then
            containerSele8.Color = backColorSeleB
            text8.Color = textColorSeleB
        End If
        If contm = 9 Then
            containerSele9.Color = backColorSeleB
            text9.Color = textColorSeleB
        End If
        If contm = 10 Then
            containerSele10.Color = backColorSeleB
            text10.Color = textColorSeleB
        End If
    End Sub

    Public Sub SeleMenuA()
        If contm <> 1 Then
            containerSele1.Color = backColorSeleA
            text1.Color = textColorSeleA
        End If
        If contm <> 2 Then
            containerSele2.Color = backColorSeleA
            text2.Color = textColorSeleA
            texton2.Color = textColorSeleA
        End If
        If contm <> 3 Then
            containerSele3.Color = backColorSeleA
            text3.Color = textColorSeleA
            texton3.Color = textColorSeleA
        End If
        If contm <> 4 Then
            containerSele4.Color = backColorSeleA
            text4.Color = textColorSeleA
        End If
        If contm <> 5 Then
            containerSele5.Color = backColorSeleA
            text5.Color = textColorSeleA
        End If
        If contm <> 6 Then
            containerSele6.Color = backColorSeleA
            text6.Color = textColorSeleA
        End If
        If contm <> 7 Then
            containerSele7.Color = backColorSeleA
            text7.Color = textColorSeleA
        End If
        If contm <> 8 Then
            containerSele8.Color = backColorSeleA
            text8.Color = textColorSeleA
        End If
        If contm <> 9 Then
            containerSele9.Color = backColorSeleA
            text9.Color = textColorSeleA
        End If
        If contm <> 10 Then
            containerSele10.Color = backColorSeleA
            text10.Color = textColorSeleA
        End If
    End Sub
    Public Sub OnTick(o As Object, e As EventArgs)
        If Player <> Nothing And Player.CanControlCharacter <> Nothing And Player.IsAlive And Player.Character <> Nothing Then

            If bImortal = True Then
                texton2.Caption = "[LIG]"
            End If
            If bImortal = False Then
                texton2.Caption = "[DES]"
            End If
            If bBlackout = True Then
                texton3.Caption = "[LIG]"
            End If
            If bBlackout = False Then
                texton3.Caption = "[DES]"
            End If

            containerFundo.Draw()
            containerTopo.Draw()
            containerSele1.Draw()
            containerSele2.Draw()
            containerSele3.Draw()
            containerSele4.Draw()
            containerSele5.Draw()
            containerSele6.Draw()
            containerSele7.Draw()
            containerSele8.Draw()
            containerSele9.Draw()
            containerSele10.Draw()
            containerSeleOn.Draw()
            containerSeleOn2.Draw()
        End If
    End Sub

    Public Sub OnKeyDown(o As Object, e As KeyEventArgs)
        If e.KeyCode = Keys.F9 Or e.KeyCode = Keys.NumPad0 And containerFundo.Enabled Or e.KeyCode = Keys.Back And containerFundo.Enabled Then
            containerFundo.Enabled = Not containerFundo.Enabled
            containerTopo.Enabled = Not containerTopo.Enabled
            containerSele1.Enabled = Not containerSele1.Enabled
            containerSele2.Enabled = Not containerSele2.Enabled
            containerSele3.Enabled = Not containerSele3.Enabled
            containerSele4.Enabled = Not containerSele4.Enabled
            containerSele5.Enabled = Not containerSele5.Enabled
            containerSele6.Enabled = Not containerSele6.Enabled
            containerSele7.Enabled = Not containerSele7.Enabled
            containerSele8.Enabled = Not containerSele8.Enabled
            containerSele9.Enabled = Not containerSele9.Enabled
            containerSele10.Enabled = Not containerSele10.Enabled
            containerSeleOn.Enabled = Not containerSeleOn.Enabled
            containerSeleOn2.Enabled = Not containerSeleOn2.Enabled

            contm = 1
            Native.Function.Call(Hash.PLAY_SOUND_FRONTEND, -1, "NAV_UP_DOWN", "HUD_FRONTEND_DEFAULT_SOUNDSET", 0)
        End If
    End Sub

    Public Sub LoadMenu()

        containerFundo = New UIContainer(New Point(5 * 200, 40), New Size(PANEL_WIDTH, PANEL_HEIGHTF), backColorFundo)
        containerTopo = New UIContainer(New Point(5 * 200, 40), New Size(PANEL_WIDTH, PANEL_HEIGHTT), backColorTopo)
        containerSele1 = New UIContainer(New Point(5 * 200, 115), New Size(PANEL_WIDTH, PANEL_HEIGHTS), backColorSeleA)
        containerSele2 = New UIContainer(New Point(5 * 200, 150), New Size(PANEL_WIDTH, PANEL_HEIGHTS), backColorSeleA)
        containerSeleOn = New UIContainer(New Point(5 * 200, 150), New Size(PANEL_WIDTH, PANEL_HEIGHTS), backColorSeleOn)
        containerSele3 = New UIContainer(New Point(5 * 200, 185), New Size(PANEL_WIDTH, PANEL_HEIGHTS), backColorSeleA)
        containerSeleOn2 = New UIContainer(New Point(5 * 200, 185), New Size(PANEL_WIDTH, PANEL_HEIGHTS), backColorSeleOn)
        containerSele4 = New UIContainer(New Point(5 * 200, 220), New Size(PANEL_WIDTH, PANEL_HEIGHTS), backColorSeleA)
        containerSele5 = New UIContainer(New Point(5 * 200, 255), New Size(PANEL_WIDTH, PANEL_HEIGHTS), backColorSeleA)
        containerSele6 = New UIContainer(New Point(5 * 200, 290), New Size(PANEL_WIDTH, PANEL_HEIGHTS), backColorSeleA)
        containerSele7 = New UIContainer(New Point(5 * 200, 325), New Size(PANEL_WIDTH, PANEL_HEIGHTS), backColorSeleA)
        containerSele8 = New UIContainer(New Point(5 * 200, 360), New Size(PANEL_WIDTH, PANEL_HEIGHTS), backColorSeleA)
        containerSele9 = New UIContainer(New Point(5 * 200, 395), New Size(PANEL_WIDTH, PANEL_HEIGHTS), backColorSeleA)
        containerSele10 = New UIContainer(New Point(5 * 200, 430), New Size(PANEL_WIDTH, PANEL_HEIGHTS), backColorSeleA)

        Titulo = New UIText("", New Point(PANEL_WIDTH / 2, 25), 0.65F, textColorTopo, GTA.Font.HouseScript, True)
        text1 = New UIText("", New Point(PANEL_WIDTH / 4, 8), 0.35F, textColorSeleA, GTA.Font.ChaletLondon, True)
        text2 = New UIText("", New Point(PANEL_WIDTH / 4.7, 8), 0.35F, textColorSeleA, GTA.Font.ChaletLondon, True)
        texton2 = New UIText("", New Point(PANEL_WIDTH / 1.2, 8), 0.35F, textColorSeleA, GTA.Font.ChaletLondon, True)
        text3 = New UIText("", New Point(PANEL_WIDTH / 4.2, 8), 0.35F, textColorSeleA, GTA.Font.ChaletLondon, True)
        texton3 = New UIText("", New Point(PANEL_WIDTH / 1.2, 8), 0.35F, textColorSeleA, GTA.Font.ChaletLondon, True)
        text4 = New UIText("", New Point(PANEL_WIDTH / 6, 8), 0.35F, textColorSeleA, GTA.Font.ChaletLondon, True)
        text5 = New UIText("", New Point(PANEL_WIDTH / 6, 8), 0.35F, textColorSeleA, GTA.Font.ChaletLondon, True)
        text6 = New UIText("", New Point(PANEL_WIDTH / 6, 8), 0.35F, textColorSeleA, GTA.Font.ChaletLondon, True)
        text7 = New UIText("", New Point(PANEL_WIDTH / 6, 8), 0.35F, textColorSeleA, GTA.Font.ChaletLondon, True)
        text8 = New UIText("", New Point(PANEL_WIDTH / 6, 8), 0.35F, textColorSeleA, GTA.Font.ChaletLondon, True)
        text9 = New UIText("", New Point(PANEL_WIDTH / 6, 8), 0.35F, textColorSeleA, GTA.Font.ChaletLondon, True)
        text10 = New UIText("", New Point(PANEL_WIDTH / 6, 8), 0.35F, textColorSeleA, GTA.Font.ChaletLondon, True)

        containerTopo.Items.Add(Titulo)
        containerSele1.Items.Add(text1)
        containerSele2.Items.Add(text2)
        containerSeleOn.Items.Add(texton2)
        containerSele3.Items.Add(text3)
        containerSeleOn2.Items.Add(texton3)
        containerSele4.Items.Add(text4)
        containerSele5.Items.Add(text5)
        containerSele6.Items.Add(text6)
        containerSele7.Items.Add(text7)
        containerSele8.Items.Add(text8)
        containerSele9.Items.Add(text9)
        containerSele10.Items.Add(text10)

        Titulo.Caption = "TRAINER BETA 1.1"
        text1.Caption = "METEOROS"
        text2.Caption = "INCENCÍVEL"
        text3.Caption = "BLACKOUT"
        text4.Caption = "NULL"
        text5.Caption = "NULL"
        text6.Caption = "NULL"
        text7.Caption = "NULL"
        text8.Caption = "NULL"
        text9.Caption = "NULL"
        text10.Caption = "NULL"

    End Sub
End Class
