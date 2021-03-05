# SPDX-License-Identifier: GPL-2.0
ccflags-y := -Idrivers/gpu/drm/msm
ccflags-$(CONFIG_DRM_MSM_DSI) += -Idrivers/gpu/drm/msm/dsi

msm_drm-y := \
	dp/dp_usbpd.o \
	dp/dp_parser.o \
	dp/dp_power.o \
	dp/dp_catalog.o \
	dp/dp_catalog_v420.o \
	dp/dp_catalog_v200.o \
	dp/dp_aux.o \
	dp/dp_panel.o \
	dp/dp_link.o \
	dp/dp_ctrl.o \
	dp/dp_audio.o \
	dp/dp_debug.o \
	dp/dp_mst_sim_helper.o \
	dp/dp_mst_sim.o \
	dp/dp_hpd.o \
	dp/dp_aux_bridge.o \
	dp/dp_bridge_hpd.o \
	dp/dp_gpio_hpd.o \
	dp/dp_lphw_hpd.o \
	dp/dp_display.o \
	dp/dp_drm.o \
	dp/dp_hdcp2p2.o \
	dp/dp_mst_drm.o \
	sde/sde_crtc.o \
	sde/sde_encoder.o \
	sde/sde_encoder_phys_vid.o \
	sde/sde_encoder_phys_cmd.o \
	sde/sde_irq.o \
	sde/sde_core_irq.o \
	sde/sde_core_perf.o \
	sde/sde_rm.o \
	sde/sde_kms_utils.o \
	sde/sde_kms.o \
	sde/sde_plane.o \
	sde/sde_connector.o \
	sde/sde_color_processing.o \
	sde/sde_vbif.o \
	sde_io_util.o \
	sde/sde_hw_reg_dma_v1_color_proc.o \
	sde/sde_hw_color_proc_v4.o \
	sde/sde_hw_ad4.o \
	sde_edid_parser.o \
	sde_hdcp_1x.o \
	sde_hdcp_2x.o \
	xiaomi_frame_stat.o

msm_drm-$(CONFIG_DEBUG_FS) += sde_dbg.o \
	sde_dbg_evtlog.o \

msm_drm-$(CONFIG_DRM_MSM_HDMI) += hdmi/hdmi.o \
	hdmi/hdmi_audio.o \
	hdmi/hdmi_bridge.o \
	hdmi/hdmi_connector.o \
	hdmi/hdmi_i2c.o \
	hdmi/hdmi_phy.o \
	hdmi/hdmi_phy_8960.o \
	hdmi/hdmi_phy_8x60.o \
	hdmi/hdmi_phy_8x74.o \
	edp/edp.o \
	edp/edp_aux.o \
	edp/edp_bridge.o \
	edp/edp_connector.o \
	edp/edp_ctrl.o \
	edp/edp_phy.o \
	mdp/mdp_format.o \
	mdp/mdp_kms.o \
	mdp/mdp4/mdp4_crtc.o \
	mdp/mdp4/mdp4_dtv_encoder.o \
	mdp/mdp4/mdp4_lcdc_encoder.o \
	mdp/mdp4/mdp4_lvds_connector.o \
	mdp/mdp4/mdp4_irq.o \
	mdp/mdp4/mdp4_kms.o \
	mdp/mdp4/mdp4_plane.o \
	mdp/mdp5/mdp5_cfg.o \
	mdp/mdp5/mdp5_ctl.o \
	mdp/mdp5/mdp5_crtc.o \
	mdp/mdp5/mdp5_encoder.o \
	mdp/mdp5/mdp5_irq.o \
	mdp/mdp5/mdp5_mdss.o \
	mdp/mdp5/mdp5_kms.o \
	mdp/mdp5/mdp5_pipe.o \
	mdp/mdp5/mdp5_mixer.o \
	mdp/mdp5/mdp5_plane.o \
	mdp/mdp5/mdp5_smp.o \
	msm_atomic.o \
	msm_debugfs.o \
	msm_drv.o \
	msm_fb.o \
	msm_fence.o \
	msm_gem.o \
	msm_gem_prime.o \
	msm_gem_shrinker.o \
	msm_gem_submit.o \
	msm_gem_vma.o \
	msm_gpu.o \
	msm_iommu.o \
	msm_perf.o \
	msm_rd.o \
	msm_ringbuffer.o

msm-$(CONFIG_DRM_FBDEV_EMULATION) += msm_fbdev.o
msm-$(CONFIG_COMMON_CLK) += mdp/mdp4/mdp4_lvds_pll.o
msm-$(CONFIG_COMMON_CLK) += hdmi/hdmi_pll_8960.o
msm-$(CONFIG_COMMON_CLK) += hdmi/hdmi_phy_8996.o

msm-$(CONFIG_DRM_MSM_HDMI_HDCP) += hdmi/hdmi_hdcp.o

msm-$(CONFIG_DRM_MSM_DSI) += dsi/dsi.o \
			mdp/mdp4/mdp4_dsi_encoder.o \
			dsi/dsi_cfg.o \
			dsi/dsi_host.o \
			dsi/dsi_manager.o \
			dsi/phy/dsi_phy.o \
			mdp/mdp5/mdp5_cmd_encoder.o

msm-$(CONFIG_DRM_MSM_DSI_28NM_PHY) += dsi/phy/dsi_phy_28nm.o
msm-$(CONFIG_DRM_MSM_DSI_20NM_PHY) += dsi/phy/dsi_phy_20nm.o
msm-$(CONFIG_DRM_MSM_DSI_28NM_8960_PHY) += dsi/phy/dsi_phy_28nm_8960.o
msm-$(CONFIG_DRM_MSM_DSI_14NM_PHY) += dsi/phy/dsi_phy_14nm.o

ifeq ($(CONFIG_DRM_MSM_DSI_PLL),y)
msm-y += dsi/pll/dsi_pll.o
msm-$(CONFIG_DRM_MSM_DSI_28NM_PHY) += dsi/pll/dsi_pll_28nm.o
msm-$(CONFIG_DRM_MSM_DSI_28NM_8960_PHY) += dsi/pll/dsi_pll_28nm_8960.o
msm-$(CONFIG_DRM_MSM_DSI_14NM_PHY) += dsi/pll/dsi_pll_14nm.o
endif

obj-$(CONFIG_DRM_MSM)	+= msm.o
