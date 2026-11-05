/**
 * Gray_one
 * Cool gray surfaces with a yellow accent.
 */

/// <reference types="@valenced/themes-api" />

import { lazyColors } from '../../../shared/theme-kit'
import type { Look, Palette, Tone } from '../../../shared/theme-kit'

const yellow = '#f5c542'
const silver = '#c0c0c0'

function withAlpha(color: string, alpha: string): string
{
	return color + alpha
}

function buildTone(): Tone
{
	return {
		greys: [
			['#2c2d32', '#161a1d'],
			['#323339', '#212529'],
			['#393a41', '#2a2f33'],
			['#3f4048', '#2f353a'],
			['#595a63', '#4a5057'],
			['#abacb2', '#a8a8a8'],
			['#c5c6ca', '#d3d3d3'],
			['#f3f3f4', '#f0f0f0'],
		],
		hues: {
			red: '#ed4245',
			orange: '#faa61a',
			yellow: yellow,
			green: '#3ba55d',
			teal: silver,
			blue: silver,
			blurple: yellow,
			purple: silver,
			pink: silver,
		},
	}
}

function buildPalette(): Palette
{
	return {
		rail: '#161a1d',
		floor: '#212529',
		panel: '#1c2024',
		page: '#212529',
		card: '#212529',
		popup: '#212529',
		input: '#2a2d31',
		control: '#2a2f33',
		pressed: '#2a2d31',

		heading: '#e3e3e3',
		strong: '#f0f0f0',
		text: '#f0f0f0',
		subtle: '#d3d3d3',
		muted: '#a8a8a8',
		faint: '#646668',

		divider: '#2c3035',
		border: '#2c3035',
		borderStrong: '#53565a',

		accent: yellow,
		accentPress: '#d0a738',
		onAccent: '#000000',
		accentSoft: withAlpha(yellow, '30'),
		accentText: yellow,
		brand: yellow,
		rowIcon: '#b4b4b4',
		selection: '#2a2d31',

		link: silver,
		mentionText: yellow,
		mentionPill: withAlpha(yellow, '30'),
		mentionBg: withAlpha(yellow, '1a'),
		replyBg: withAlpha(silver, '1a'),
		keyword: withAlpha(yellow, '33'),
		code: '#1c2024',
		codeText: '#f0f0f0',
		spoiler: '#2a2f33',
		spoilerRevealed: '#212529',

		positive: '#3ba55d',
		warning: '#faa61a',
		danger: '#ed4245',
		dangerFill: '#c9343c',
		scrim: '#000000b3',
	}
}

function buildLook(): Look
{
	return {
		palette: buildPalette(),
		extra: {
			CONTROL_PRIMARY_BORDER_DEFAULT: '#ffffff33',
			MOBILE_BACKGROUND_SCRIM_OPAQUE: '#000000',
			BACKGROUND_SCRIM_LIGHTBOX: '#000000f2',
			OVERLAY_BACKDROP_LIGHTBOX: '#000000f2',
		},
	}
}

export default plugin({
	preInit({ themes })
	{
		const look = buildLook()
		const about = 'Cool gray surfaces, yellow accent.'

		themes.registerGroup('gray_one', { name: 'Gray_one', description: about })
		themes.registerTheme('gray_one', 'gray_one', {
			name: 'Gray_one',
			description: about,
			background: { path: 'assets/gray-mono-wallpaper.png', blur: 4, dimming: 0.7 },
			getColors: lazyColors(buildTone(), {
				dark: look,
				darker: look,
				midnight: look,
			}),
		})
	},
})
