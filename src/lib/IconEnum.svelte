<script lang="ts" module>
	export enum Icon {
		Home,
		Config,
		Study,
		Dark_Theme,
		Light_Theme,
		Contact
	}

	export function link_of_icon(i: Icon) {
		if (i == Icon.Home) {
			return '/';
		}
		if (i == Icon.Config) {
			return '/settings';
		}
		if (i == Icon.Study) {
			return '/coursework';
		}
		if (i == Icon.Contact) {
			return '/contact';
		}
		return '/';
	}

	export function text_of_icon(i: Icon) {
		if (i == Icon.Home) {
			return 'Home';
		}
		if (i == Icon.Config) {
			return 'Settings';
		}
		if (i == Icon.Study) {
			return 'Courses';
		}
		if (i == Icon.Contact) {
			return 'Contact Me!';
		}
		return '';
	}
</script>
