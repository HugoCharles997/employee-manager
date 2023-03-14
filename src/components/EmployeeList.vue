<!-- <template>
	<div>
		<md-table>
			<md-table-row>
				<md-table-head md-numeric>ID</md-table-head>
				<md-table-head>Name</md-table-head>
				<md-table-head>Email</md-table-head>
				<md-table-head>Gender</md-table-head>
				<md-table-head>Job Title</md-table-head>
			</md-table-row>

			<md-table-row>
				<md-table-cell md-numeric>1</md-table-cell>
				<md-table-cell>Shawna Dubbin</md-table-cell>
				<md-table-cell>sdubbin0@geocities.com</md-table-cell>
				<md-table-cell>Male</md-table-cell>
				<md-table-cell>Assistant Media Planner</md-table-cell>
			</md-table-row>

			<md-table-row>
				<md-table-cell md-numeric>2</md-table-cell>
				<md-table-cell>Odette Demageard</md-table-cell>
				<md-table-cell>odemageard1@spotify.com</md-table-cell>
				<md-table-cell>Female</md-table-cell>
				<md-table-cell>Account Coordinator</md-table-cell>
			</md-table-row>

			<md-table-row>
				<md-table-cell md-numeric>3</md-table-cell>
				<md-table-cell>Vera Taleworth</md-table-cell>
				<md-table-cell>vtaleworth2@google.ca</md-table-cell>
				<md-table-cell>Male</md-table-cell>
				<md-table-cell>Community Outreach Specialist</md-table-cell>
			</md-table-row>
		</md-table>
	</div>
</template>

<script>
export default {
	name: "TableBasic",
};
</script> -->

<template>
	<div>
		<md-table>
			<md-table-row>
				<md-table-head md-numeric>ID</md-table-head>
				<md-table-head>Name</md-table-head>
				<md-table-head>Email</md-table-head>
				<md-table-head>Gender</md-table-head>
				<md-table-head>Job Title</md-table-head>
			</md-table-row>
			<md-table-row v-for="user in users" :key="user.id">
				<md-table-cell md-numeric>{{ user.id }}</md-table-cell>
				<md-table-cell>{{ user.name }}</md-table-cell>
				<md-table-cell>{{ user.email }}</md-table-cell>
				<md-table-cell>{{ user.gender }}</md-table-cell>
				<md-table-cell>{{ user.jobTitle }}</md-table-cell>
			</md-table-row>
		</md-table>
	</div>
</template>
<script>
export default {
	name: "TableBasic",
	data() {
		return {
			users: [
				{
					id: 1,
					name: "Shawna Dubbin",
					email: "sdubbin0@geocities.com",
					gender: "Male",
					jobTitle: "Assistant Media Planner",
				},
				{
					id: 2,
					name: "Odette Demageard",
					email: "odemageard1@spotify.com",
					gender: "Female",
					jobTitle: "Account Coordinator",
				},
				{
					id: 3,
					name: "Vera Taleworth",
					email: "vtaleworth2@google.ca",
					gender: "Male",
					jobTitle: "Community Outreach Specialist",
				},
			],
		};
	},
};
</script>
